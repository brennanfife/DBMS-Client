<script>
export let item = {};
</script>
<style>
    .userProfilePic {
        border-radius: 50%;
    }
</style>
<div class="box">
  <article class="media">
    <div class="media-left">
      <figure class="image is-64x64 userProfilePic">
        <img src="https://bulma.io/images/placeholders/128x128.png" alt="Image">
      </figure>
    </div>
    <div class="media-content">
      <div class="content">
        <p>
          <strong>{item.userName}</strong> Voted: 
          <br>
          {item.resName}
        </p>
      </div>
    </div>
  </article>
</div>
