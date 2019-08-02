<script>
  import ResCard from "../components/ResCard.svelte";
  import Polling from "./Polling.svelte";
  import ResLanding from "./ResLanding.svelte";
  import { Router, Link, Route } from "svelte-routing";
</script>

<style>
  .custom-padding {
    padding: 30px;
  }
  .columns {
    background-color: white;
    margin: 0;
    height: 100%;
  }
  .column {
    overflow-y: scroll;
  }
  .landing-search {
    height: 100%;
    background: radial-gradient(
        circle closest-side at 50px 50px,
        #fb8b24 3px,
        transparent 0
      ),
      radial-gradient(
        circle closest-side at 40px 60px,
        #fb8b24 3px,
        transparent 0
      ),
      radial-gradient(
        circle closest-side at 60px 60px,
        #fb8b24 3px,
        transparent 0
      ),
      radial-gradient(
        circle closest-side at 50px 70px,
        #fb8b24 3px,
        transparent 0
      ),
      radial-gradient(
        circle closest-side at 150px 165px,
        #fb8b24 3px,
        transparent 0
      ),
      radial-gradient(
        circle closest-side at 140px 175px,
        #fb8b24 3px,
        transparent 0
      ),
      radial-gradient(
        circle closest-side at 160px 175px,
        #fb8b24 3px,
        transparent 0
      ),
      radial-gradient(
        circle closest-side at 150px 185px,
        #fb8b24 3px,
        transparent 0
      ),
      radial-gradient(
        ellipse closest-side at 50px 60px,
        #f9a734 18px,
        transparent 0
      ),
      radial-gradient(
        ellipse closest-side at 150px 175px,
        #f9a734 18px,
        transparent 0
      ),
      radial-gradient(
        circle closest-side at 30px 40px,
        #f9d8d4 15px,
        transparent 0
      ),
      radial-gradient(
        circle closest-side at 40px 35px,
        #36964c 15px,
        transparent 0
      ),
      radial-gradient(
        circle closest-side at 70px 40px,
        #f9d8d4 15px,
        transparent 0
      ),
      radial-gradient(
        circle closest-side at 60px 35px,
        #286e38 15px,
        transparent 0
      ),
      radial-gradient(
        circle closest-side at 130px 155px,
        #f9d8d4 15px,
        transparent 0
      ),
      radial-gradient(
        circle closest-side at 140px 150px,
        #36964c 15px,
        transparent 0
      ),
      radial-gradient(circle at 170px 155px, #f9d8d4 15px, transparent 0),
      radial-gradient(circle at 160px 150px, #286e38 15px, transparent 0);
    background-color: #f9d8d4;
    background-size: 180px 210px;
  }
  .landing-address {
    height: 50px;
    width: 700px;
    font-size: 20px;
    display: inline-block;
    margin: 0;
  }
  .landing-submit {
    height: 50px;
    display: inline-block;
    margin: 0;
  }
  .landing-input {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: fit-content;
    text-align: left;
  }
  input[type="submit"] {
    font-family: FontAwesome;
  }

</style>

<div class="landing-search">
  <form class="landing-input">
    <input
      class="input is-rounded landing-address"
      type="text"
      placeholder="Search Madison's Resturaunts..." />
    <!-- <input type="submit" class="landing-submit"> -->
    <input
      class="button is-danger is-rounded is-medium"
      type="submit"
      value="&#xf002" />

  </form>
</div>
