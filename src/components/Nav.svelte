<script>
  import { Router, Link } from "svelte-routing";
  import Polling from "../pages/Polling.svelte";
  import ResLanding from "../pages/ResLanding.svelte";
  export let links = [];
  export let linkFloat = "";
</script>

<style>
  .nav {
    height: 70px;
    background-color: white;
    box-shadow: 1px 5px 4px 0 rgba(0, 0, 0, 0.1);
    position: relative;
    z-index: 1000;
  }
  .nav-options {
    display: inline-block;
    padding: 20px 20px;
    height: 100%;
    min-width: 100px;
    text-align: center;
  }
  .right {
    float: right;
  }
  .middle {
    text-align: center;
  }
</style>

<nav class="nav {linkFloat}">
  {#each links as navOptionInfo}
    <div class="nav-options {navOptionInfo.position}">
      <Link to={navOptionInfo.url}>{navOptionInfo.name}</Link>
    </div>
  {/each}
</nav>
