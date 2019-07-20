<script>
  import {Router, Link} from "svelte-routing";
  import Polling from "../pages/Polling.svelte";
</script>
<style>
.nav {
  height: 70px;
  background-color: white;
  box-shadow: -2px -1px 7px #777777c2;
  z-index: 100000;
}
.nav-options {
  display: inline-block;
  padding: 20px 20px;
  height: 100%;
  min-width: 100px;
    text-align: center;
}

.nav-link {
  text-decoration: none;
  display: inline-block;
}

.nav-logo {
  height: 20px;
  width: 20px;
}
</style>



<nav class="nav">
  <img src="imgur.com/vegSDte" alt="hhh" class="nav-logo">
  <div class="nav-options"><Link to="/home">Home</Link></div>
  <div class="nav-options"><Link to="/polling">Polling</Link></div>
  <div class="nav-options"><Link to="/profile">Profile</Link></div>
</nav>