<script>
  export let isPolling;
</script>


<style>
    .card-mod {
        width: calc( (100% - 40px)  / 2);
        box-sizing: border-box;
        display: inline-block;
        margin-bottom: 20px;
    }
    .card-stat, .card-action {
      display: block;
      text-align: center;
      width: 100%;
    }
    .card-footer-item {
      flex-wrap: wrap;
    }
</style>

<div class="card card-mod">
  <div class="card-image">
    <figure class="image is-4by3">
      <img src="https://bulma.io/images/placeholders/1280x960.png" alt="Placeholder image">
    </figure>
  </div>
  <div class="card-content">
    <div class="media">
      <div class="media-content">
        <p class="title is-4">John Smith</p>
        <p class="subtitle is-6">@johnsmith</p>
      </div>
    </div>

    <div class="content">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit.
      Phasellus nec iaculis mauris. <a>@bulmaio</a>.
      <a href="#">#css</a> <a href="#">#responsive</a>
      <br>
      <time datetime="2016-1-1">11:09 PM - 1 Jan 2016</time>
    </div>
  </div>
  {#if isPolling}
  <footer class="card-footer">
    <a href="#" class="card-footer-item"><span class="card-action">Up</span><span class="card-stat">36</span></a>
    <a href="#" class="card-footer-item"><span class="card-action">Down</span><span class="card-stat">36</span></a>
  </footer>
  {/if}
</div>