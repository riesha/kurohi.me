<script>
</script>

<div class="nav">
  <div class="nav-list">
    <a href="/">home</a>
    <a href="/projects">projects</a>
    <a href="/about">about</a>
  </div>
</div>

<style>
  .nav {
    padding: 5px;
    background: rgb(31, 31, 31);
    border: 1px solid #9e77be;
    border-radius: 2px;
    margin: 5px;
    font-size: 0.9em;
  }
  a {
    color: #cc9bf5;
  }
  a:not(:last-child)::after {
    content: "†";
    margin-inline: 0.5rem;
  }
  .nav-list:last-child::after {
    content: '☆○o｡..:*･"†';
    margin-inline: 0.5rem;
  }
  .nav-list:first-child::before {
    content: "†ﾟ¨ﾟﾟ･:..☆";
    margin-inline: 0.5rem;
  }
  @media (max-width: 576px) {
    .nav-list:last-child::after {
      content: "☆";
    }
    .nav-list:first-child::before {
      content: "☆";
    }
  }
</style>
