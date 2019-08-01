<script>
    import ResCard from "../components/ResCard.svelte";
    import UserPollingCard from "../components/UserPollingCard.svelte";
    let userVotes = [
        {
            userName: "Donglin",
            resName: "Crabby Burger"
        },
        {
            userName: "hahahahah",
            resName: "Crabby Burger"
        },
    ]

    let resInfo = [
        {
            imgURL: "http://lorempixel.com/640/480/food",
            resName: "Cento",
            resDescription: "Fancy",
        },
        {
            imgURL: "http://lorempixel.com/640/480/food",
            resName: "Hooyah",
            resDescription: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed eget sem lacus. Suspendisse at nibh sagittis, dignissim purus sed, tempor ex. Ut in luctus felis. Duis vel purus rhoncus, dapibus diam non, maximus nulla. ",
        },
        {
            imgURL: "http://lorempixel.com/640/480/food",
            resName: "Ramen Nation",
            resDescription: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed eget sem lacus. Suspendisse at nibh sagittis, dignissim purus sed, tempor ex. Ut in luctus felis. Duis vel purus rhoncus, dapibus diam non, maximus nulla. ",
        }, 
        {
            imgURL: "http://lorempixel.com/640/480/food",
            resName: "Sushi Express",
            resDescription: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed eget sem lacus. Suspendisse at nibh sagittis, dignissim purus sed, tempor ex. Ut in luctus felis. Duis vel purus rhoncus, dapibus diam non, maximus nulla. ",
        },
    ]

</script>

<style>
  .columns {
    margin: 0;
    height: 100%;
  }
  .column {
    overflow-y: scroll;
  }
</style>

<div class="columns ">
  <div class="column is-three-fifths">
    {#each resInfo as resCard}
        <ResCard isPolling={true} resInfo={resCard} />
    {/each}
  </div>
  <div class="column">
    {#each userVotes as userCard}
        <UserPollingCard item={userCard} />
    {/each}
  </div>
</div>
