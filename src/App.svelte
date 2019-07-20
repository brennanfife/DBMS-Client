<script>
  import { Router, Link, Route } from "svelte-routing";
  import Test from "./components/Test.svelte";
  import Polling from "./pages/Polling.svelte";
  import Home from "./pages/Home.svelte";
  import Nav from "./components/Nav.svelte";
</script>

<style>
  .main-container {
    margin-top: 10px;
  }
</style>

<Router url="">

  <Nav />
  <div class="main-container">
    <Route path="/" component={Test} />
    <Route path="polling" component={Polling} />
    <Route path="home" component={Home} />
  </div>

</Router>
