<script>
  import { Router, Link, Route } from "svelte-routing";
  import Polling from "./pages/Polling.svelte";
  import Home from "./pages/Home.svelte";
  import Nav from "./components/Nav.svelte";
  import ResLanding from "./pages/ResLanding.svelte";
  import Profile from "./pages/Profile.svelte";
  import Login from "./pages/Login.svelte";
  import Register from "./pages/Register.svelte";
  const navOptions = [
    { name: "Home", url: "/home", position: "" },
    { name: "Polling", url: "/polling", position: "" },
    { name: "Profile", url: "/profile", position: "" },
    { name: "Log in", url: "/login", position: "right" },
    { name: "Sign up", url: "/register", position: "right" }
  ];
</script>

<style>
  .main-container {
    /* margin-top: 10px; */
    background-color: white;
    height: calc(100vh - 70px);
    z-index: 0;
  }
</style>

<Router url="">
  <Nav links={navOptions} />
  <div class="main-container">
    <Route path="/*" component={Home} />
    <Route path="polling" component={Polling} /> 
    <Route path="profile/*" component={Profile} />
    <Route path="login" component={Login} />
    <Route path="login/:fromRegister" component={Login} />
    <Route path="register" component={Register} />
  </div>
</Router>
