<script>
  export let name;
  export let description;
  export let language;
  export let stack;
  export let link;
  let showmore = false;
  import { fade } from "svelte/transition";
</script>

<div class="project">
  <div class="name"><p>{name}</p></div>
  <vl />
  <div class="description"><p>{description}</p></div>

  <!-- {#if !showmore}
      <p>&gt;</p>
    {:else}
      <p>&lt;</p>{/if} -->
  <div class="link"><a href={link}>🔗</a></div>

  <div class="extras">{language} {stack.length > 0 ? "-" : ""} {stack}</div>
</div>

<style>
  .project {
    border: 1px solid #9e77be;
    border-radius: 2px;
    min-height: 50px;
    display: flex;
    padding: 5px;
    box-shadow: black 0px 5px 10px;
    position: relative;
    margin-bottom: 10px;
    overflow-wrap: break-word;
  }
  vl {
    border: 1px solid #9e77be;
    border-radius: 1px;
  }
  .name {
    margin-top: auto;
    margin-bottom: auto;
    min-width: 10rem;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .link {
    margin-top: auto;
    margin-left: auto;
    margin-right: 1rem;
    margin-bottom: auto;
  }
  .extras {
    font-size: 0.8em;
    font-family: "basiic";
    width: 100%;
    padding: 0;
    margin: 5px;
    display: flex;
    width: fit-content;
    text-align: right;
    justify-content: center;
    align-items: center;
    margin-left: auto;
    color: hsl(0, 0%, 50%);
  }
  .description {
    margin-top: auto;
    margin-bottom: auto;
    font-size: 85%;
    overflow: hidden;
  }
  a {
    cursor: pointer;
    text-align: center;
  }
</style>
