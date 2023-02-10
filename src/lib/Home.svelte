<script>
  import { fade } from "svelte/transition";
  let cat = "../assets/cat.gif";
</script>

<div class="content" in:fade>
  <h2>Home</h2>
  <p>
    Welcome to my personal website, i'm sorry for wasting your time as it's
    quite empty right now, but i plan on adding content to it over time.
  </p>
  <p>Please enjoy your time here.</p>
  <p>
    If you need any freelance dev work done and you think i'm capable of it,
    please contact me via Twitter! rates are negociable.
  </p>

  <img src="assets/barunson.gif" alt="barunson gif" />
  <hr />
  <img src="assets/witch.gif" alt="protected by witchcraft" />
  <img src="assets/cat.gif" alt="i'm a cat person" />

  <img src="assets/friends.gif" alt="i love my friends" />
  <br />
  <a href="https://osu.ppy.sh/beatmapsets/74277#osu/233068">
    <img
      class="clickable"
      src="assets/maydayb.png"
      alt="mayday b fan banner"
    /></a
  >
  <br />
  <img src="assets/buttons/kurohi1.gif" alt="kurohi.me button" />
</div>

<style>
  .content {
    padding: 5px;
    /* background: #fcf1f6; */
    border: 1px solid #9e77be;
    border-radius: 2px;
    margin: 5px;
    font-size: 0.9em;
    height: 80%;
    overflow: auto;
  }
</style>
