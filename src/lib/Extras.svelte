<script>
  import { fade } from "svelte/transition";
  let cat = "../assets/cat.gif";
</script>

<div class="content" in:fade />

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
