<script>
  import ResCard from "../components/ResCard.svelte";
  import Nav from "../components/Nav.svelte";
  import UserPollingCard from "../components/UserPollingCard.svelte";
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
    <ResCard isPolling={true} />
    <ResCard isPolling={true} />
    <ResCard isPolling={true} />
    <ResCard isPolling={true} />
  </div>
  <div class="column is-half">
    <UserPollingCard />
    <UserPollingCard />
    <UserPollingCard />
    <UserPollingCard />
  </div>
</div>
