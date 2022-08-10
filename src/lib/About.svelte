<script>
  import { fade } from "svelte/transition";
</script>

<div class="content" in:fade>
  <h2>About Me</h2>
  <img alt="My profile pic" src="assets/icon.png" class="icon" />
  <p>
    Hi, I go by many aliases online and hate to stick to one but my name's
    Selene so i guess you can call me that.
  </p>
  <p>
    The internet's been my second home ever since my mom introduced me to it
    when i was a little girl, I'm a pretty forgettable person so i wont bother
    you by telling you too much about me but I like cats, music, art and
    programming, all in all i'm a pretty basic bitch, i also play games
    sometimes, mostly sims 4, osu, otome games and minecraft since i dont have
    the energy for shooters anymore.
  </p>
  <img style="float: left;" src="assets/aiko.jpg" class="icon" alt="my cat" />
  <p>
    I'm quadrilingual (english/spanish/french/catalan) and mostly code in
    rust/elixir/python/c++/js(at gunpoint). I collect artbooks (300 gigs as of
    now!) and i'm addicted to taking pictures of my cat! Her name's Aiko and you
    can find many pictures of her on my twitter below!
  </p>
  <br />
  <p>
    <i
      >That's pretty much it i guess, as you can see i'm horrible at writing
      about myself (╥﹏╥)</i
    >
  </p>
  <hr />
  <a href="https://twitter.com/lysacht">twitter</a> †
  <a href="https://github.com/riesha">github</a>
  †
  <a href="https://www.last.fm/user/lauriers">lastfm</a>
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
  .icon {
    width: 100px;
    height: 100px;
    border: 1px solid #9e77be;
    float: right;
    padding: 1px;
    margin: 5px;
  }
</style>
