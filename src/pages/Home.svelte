<script>
  import ResCard from "../components/ResCard.svelte";
  import Polling from "./Polling.svelte";
  import { Router, Link, Route } from "svelte-routing";
</script>

<style>
  .custom-padding {
    padding: 30px;
  }
  .columns {
    background-color: white;
    margin: 0;
  }
  .column {
    overflow: scroll;
    height: 100vh;
  }
</style>

  <div class="columns ">
    <div class="column is-half custom-padding">
      
        <ResCard isPolling={false}/>
        <ResCard isPolling={false}/>
        <ResCard isPolling={false}/>
        <ResCard isPolling={false}/>
        <ResCard isPolling={false}/>
    </div>
    <div class="column is-half">
      <div class="container">
      </div>
    </div>
  </div>
