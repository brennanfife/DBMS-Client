<script>
  import axios from "axios";
  import { Link, navigate } from "svelte-routing";
  const registerRouteSubfix = "/api/user/register";
  let hasWarning = false;
  let warningMessage = "";
  const handleLogin = event => {
    let { name, email, password, password2 } = event.target;
    axios
      .post("http://localhost:8460/api/user/register", {
        name: name.value,
        email: email.value,
        password: password.value,
        password2: password2.value
      })
      .then(res => {
        if (res.data.error) {
          hasWarning = true;
          warningMessage = res.data.error;
        } else {
            navigate('/login/fromRegister', {replace: true});
        }
      })
      .catch(err => {
        console.error(err);
      });
  };
</script>

<style>
  .login {
    height: 100%;
    width: 100%;
    padding: 70px 0;
    text-align: center;
  }
  .login-block {
    width: 400px;
    display: inline-block;
  }
  .login-title {
    font-weight: 700;
    font-size: 40px;
    margin-bottom: 20px;
  }
  .login-group {
    display: block;
  }
  .login-group:not(first-child) {
    margin-top: 10px;
  }
  .login-label {
    font-size: 20px;
    text-align: left;
  }
  .login-input {
    width: 100%;
    height: 50px;
    font-size: 20px;
  }
  .login-input:focus {
    border-color: rgb(57, 95, 207);
  }
  .login-button {
    width: 100%;
    margin-top: 20px;
    height: 50px;
  }
  .login-link {
    margin-top: 15px;
    text-decoration: none;
  }
  .message-header {
    border-radius: 5px;
  }
</style>

<section class="login">

  <div class="login-title">Fuck me this is fuck</div>
  <form class="login-block" on:submit|preventDefault={handleLogin}>
    {#if hasWarning}
      <div class="message is-warning">
        <div class="message-header">
          <p>{warningMessage}</p>
        </div>
      </div>
    {/if}
    <div class="login-group">
      <label for="name" class="login-label">Name</label>
      <input name="name" type="text" class="login-input" />
    </div>
    <div class="login-group">
      <label for="email" class="login-label">Email</label>
      <input name="email" type="text" class="login-input" />
    </div>
    <div class="login-group">
      <label for="password" class="login-label">Password</label>
      <input name="password" type="password" class="login-input" />
    </div>
    <div class="login-group">
      <label for="password2" class="login-label">Confirm Password</label>
      <input name="password2" type="password" class="login-input" />
    </div>
    <div class="login-link">
      <Link to="/login">Have an account? Log in here</Link>
    </div>
    <div class="login-actions">
      <input type="submit" class="login-button" />
    </div>
  </form>
</section>
