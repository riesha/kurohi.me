<script>
  import router from "page";
  import About from "./lib/About.svelte";
  import Home from "./lib/Home.svelte";
  import Nav from "./lib/Nav.svelte";
  import { fade } from "svelte/transition";
  import Footer from "./lib/Footer.svelte";
  import Projects from "./lib/Projects.svelte";
  import { onMount } from "svelte";
  import Extras from "./lib/Extras.svelte";

  let url = ``;

  onMount(() => (url = window.location.href));
  let page;
  router("/", () => (page = Home));
  router("/projects", () => (page = Projects));
  router("/about", () => (page = About));
  router("/extras", () => (page = Extras));
  router.start();
</script>

<meta content="#9e77be" data-react-helmet="true" name="theme-color" />
<meta name="twitter:card" content="summary_large_image" />
<body>
  <center
    ><main>
      <h2>Welcome to my homepage!</h2>
      <Nav />

      <svelte:component this={page} />
      <Footer />
    </main></center
  >
</body>

<style>
  :global(*) {
    cursor: url("cursor.gif"), auto !important;
  }
  :global(body) {
    background: rgb(27, 27, 27);
    color: #9e77be;
    font-family: "basiic";
  }

  @font-face {
    font-family: "basiic";
    src: url(https://cinni.net/fonts/basiic.ttf);
  }
  @font-face {
    font-family: "gohu";
    src: url("gohu.woff") format("woff");
  }
  @font-face {
    font-family: "Spirit";
    src: url("Spirit.ttf") format("truetype");
  }
  ::selection {
    background: pink;
    color: #e000c3;
  }
  main {
    margin: 0 auto;
    width: 600px;

    height: 650px;
    margin-top: 30px;
  }
  :global(.clickable) {
    cursor: url("pointer.png"), pointer !important;
  }
  :global(a) {
    cursor: url("pointer.png"), pointer !important;
    color: #9e77be;
    letter-spacing: 1px;
    text-decoration: none;
  }
  :global(a:hover) {
    color: #e07aff;
  }

  :global(hr) {
    color: #9e77be;
    border-top: 1px solid #9e77be;
    border-left: none;
    border-right: none;
    border-bottom: none;
    width: 70%;
  }
  h2 {
    /* text-transform: uppercase; */
    font-family: "Spirit";
    background: linear-gradient(
      90deg,
      rgba(249, 162, 243, 0) 0%,
      rgb(203, 144, 241) 25%,
      rgb(203, 144, 241) 75%,
      rgba(249, 162, 243, 0) 100%
    );
    font-size: 1em;
    padding: 1px;
    color: rgb(39, 39, 39);
    filter: drop-shadow(16px 16px 10px black);
    letter-spacing: 2px;
  }
  :global(.content) {
    scrollbar-width: none;
    background: rgb(31, 31, 31);
    font-family: "gohu";
  }
  :global(.content p) {
    text-align: left;
    margin: 15px;
  }
  :global(.content h1) {
    text-transform: uppercase;
    font-family: "basiic";
    background: linear-gradient(
      0deg,
      rgb(152, 119, 190) 0%,
      rgb(152, 119, 190) 6%,
      rgba(235, 183, 194, 0) 6%,
      rgba(249, 162, 243, 0) 100%
    );
    font-size: 1.2em;
    padding: 1px;
    padding-left: 12px;
    font-weight: bold;
    letter-spacing: 2px;
    text-align: left;
  }
  :global(.content h2) {
    /* text-transform: uppercase; */
    font-family: "basiic";
    background: linear-gradient(
      90deg,
      rgba(249, 162, 243, 0) 0%,
      rgb(203, 144, 241) 25%,
      rgb(203, 144, 241) 75%,
      rgba(249, 162, 243, 0) 100%
    );
    font-size: 1em;
    padding: 1px;
    color: rgb(39, 39, 39);
    letter-spacing: 2px;
  }
  @media screen and (max-width: 600px) {
    /* body {
      height: 100%;
      width: 400px;

      height: 600px;
      margin-top: 10px;
    } */
    main {
      width: 95%;
      height: 490px;
      margin-top: 75px;
    }
  }
</style>
