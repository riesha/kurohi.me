<script>
  import Project from "../elements/Project.svelte";
  import { fade } from "svelte/transition";
  import About from "./About.svelte";
  let projects = [
    {
      name: "drv-vuln-scanner",
      description: `Finds imports that could be exploited in drivers, still requires manual analysis. `,
      language: "rust",
      stack: "",
      link: "https://github.com/riesha/drv-vuln-scanner",
    },

    {
      name: "tiny-template",
      description: `A template for creating small rust binaries (nostd/nocrt)`,
      language: "rust",
      stack: "",
      link: "https://github.com/riesha/tiny-template",
    },
    {
      name: "iana",
      description: `wip x86/x64 hooking lib (windows)`,
      language: "rust",
      stack: "",
      link: "https://github.com/riesha/iana",
    },
    {
      name: "salmon",
      description: `McOsu score server and client mod, i started working on this with a friend (he does the client) because not being able to use discord bots while playing mcosu annoyed me, 
 we're still working on it and are hoping to open it to the public in the future.`,
      language: "rust/c++",
      stack: "postgres\nredis\nprometheus\ngrafana\nsentry",
      link: "https://test.dev.kurohi.me/",
    },
    {
      name: "salmon-web",
      description: `The salmon website`,
      language: "html/js/css",
      stack: "Svelte",
      link: "https://test.dev.kurohi.me/",
    },
    {
      name: "McOsu db parser",
      description: `Parses your mcosu score database and outputs it as json.`,
      language: "rust",
      stack: "",
      link: "https://github.com/riesha/mcosudb",
    },
    {
      name: "Personal site",
      description: `This website.`,
      language: "html/js/css",
      stack: "Svelte\nFirebase",
      link: "https://kurohi.me",
    },
    {
      name: "Skill's links",
      description: `Landing page i made for a friend.`,
      language: "html/css",
      stack: "TailwindCSS",
      link: "https://skill.kurohi.me/",
    },
  ];
</script>

<div class="content" in:fade>
  <h2>My Projects</h2>
  {#each projects as p, i}
    <Project {...p} />
  {/each}
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
