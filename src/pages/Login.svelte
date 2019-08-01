<script>
  import axios from "axios";
  import { Link } from "svelte-routing";
  import { loginEntry, loginEntryGoogle } from '../config/config.js';


  export let fromRegister = "";
  let warningMessage = "";

  const handleLogin = event => {
    let { email, password } = event.target;
    console.log(email);
    console.log(password);
    axios
      .post(loginEntry, {
        email: email.value,
        password: password.value
      })
      .then(res => {
        console.log(res);
        if (res.data.error) {
          warningMessage = res.data.error;
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
     background: radial-gradient(circle closest-side at 50px 50px, #FB8B24 3px, transparent 0), radial-gradient(circle closest-side at 40px 60px, #FB8B24 3px, transparent 0), radial-gradient(circle closest-side at 60px 60px, #FB8B24 3px, transparent 0), radial-gradient(circle closest-side at 50px 70px, #FB8B24 3px, transparent 0), radial-gradient(circle closest-side at 150px 165px, #FB8B24 3px, transparent 0), radial-gradient(circle closest-side at 140px 175px, #FB8B24 3px, transparent 0), radial-gradient(circle closest-side at 160px 175px, #FB8B24 3px, transparent 0), radial-gradient(circle closest-side at 150px 185px, #FB8B24 3px, transparent 0), radial-gradient(ellipse closest-side at 50px 60px, #F9A734 18px, transparent 0), radial-gradient(ellipse closest-side at 150px 175px, #F9A734 18px, transparent 0), radial-gradient(circle closest-side at 30px 40px, #F9D8D4 15px, transparent 0), radial-gradient(circle closest-side at 40px 35px, #36964C 15px, transparent 0), radial-gradient(circle closest-side at 70px 40px, #F9D8D4 15px, transparent 0), radial-gradient(circle closest-side at 60px 35px, #286E38 15px, transparent 0), radial-gradient(circle closest-side at 130px 155px, #F9D8D4 15px, transparent 0), radial-gradient(circle closest-side at 140px 150px, #36964C 15px, transparent 0), radial-gradient(circle at 170px 155px, #F9D8D4 15px, transparent 0), radial-gradient(circle at 160px 150px, #286E38 15px, transparent 0);
  background-color: #F9D8D4;
  background-size: 180px 210px;
  }
  .login-block {
    width: 400px;
    display: inline-block;
  }
  .login-title {
    font-weight: 700;
    font-size: 40px;
    margin-bottom: 20px;
    text-transform: capitalize;
    text-align: left;
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
    text-decoration: none;
  }
  .message-header {
    border-radius: 5px;
  }
</style>

<section class="login">

 
  <form class="login-block" on:submit|preventDefault={handleLogin}>
    <div class="login-title">Log In</div>
    {#if fromRegister !== ""}
      <div class="message is-success">
        <div class="message-header">
          <p>You are successfully registered. Please log in!</p>
        </div>
      </div>
    {/if}
    {#if warningMessage}
      <div class="message is-warning">
        <div class="message-header">
          <p>{warningMessage}</p>
        </div>
      </div>
    {/if}
    <div class="login-group">
      <label for="email" class="login-label">Email</label>
      <input name="email" type="text" class="login-input" />
    </div>
    <div class="login-group">
      <label for="password" class="login-label">Password</label>
      <input name="password" type="password" class="login-input" />
    </div>
    <div class="login-link">
      <Link to="/register">No account yet? Sign up here</Link>
    </div>
    <div class="login-actions">
      <input type="submit" class="login-button" />
    </div>
  </form>
  <a href="{loginEntryGoogle}">
  aaaa
  </a>
</section>
