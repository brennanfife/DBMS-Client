<script>
  export let isPolling;
  export let resInfo = {};
</script>


<style>
    .card {
        width: calc( (100% - 40px)  / 2);
        box-sizing: border-box;
        display: inline-block;
        margin: 10px;
    }
    .card-stat, .card-action {
      display: block;
      text-align: center;
      width: 100%;
    }
    .card-footer-item {
      flex-wrap: wrap;
    }
    /* .card-content {
      height: 250px;
      overflow: hidden;
    } */
    @media all and (max-width: 1000px) {
      .card {
        width: 100%;
      }
    }
</style>

<div class="card">
  <div class="card-image">
    <figure class="image is-4by3">
      <img src="{resInfo.imgURL}" alt="Placeholder image">
    </figure>
  </div>
  <div class="card-content">
    <div class="media">
      <div class="media-content">
        <p class="title is-4">{resInfo.resName}</p>
        <p class="subtitle is-6">Cuisine 1, Cuisine 2</p>
      </div>
    </div>

    <!-- <div class="content" style="height: 200px">
      {resInfo.resDescription}
      <br>
    </div> -->
  </div>
  {#if isPolling}
  <footer class="card-footer">
    <a href="#" class="card-footer-item"><span class="card-action"><ion-icon name="thumbs-up"></ion-icon></span><span class="card-stat">36</span></a>
    <a href="#" class="card-footer-item"><span class="card-action"><ion-icon name="thumbs-down"></ion-icon></span><span class="card-stat">36</span></a>
  </footer>
  {/if}
</div>