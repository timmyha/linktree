<script lang="ts">
  const links = [
    {name: 'portfolio', url: 'https://timmyha.co', icon: 'las la-landmark'},
    {name: 'twitter', url: 'https://twitter.com/tmthyha', icon: 'lab la-twitter'},
    {name: 'my blog', url: 'https://blog.timmyha.co', icon: 'las la-rss'},
    {name: 'github', url: 'https://github.com/timmyha', icon: 'lab la-github'},
    {name: 'instagram', url: 'https://instagram.com/fordf150fansonly', icon: 'lab la-instagram'},
    {name: 'film logs', url: 'https://letterboxd.com/timmyha', icon: 'las la-film'},
    {name: 'my dot files', url: 'https://github.com/timmyha/dots', icon: 'las la-ellipsis-h'},
  ]

  const goToUrl = (link: string) => window.location.href = link
</script>

<main>
  <h1>timmyha</h1>
    {#each links as link (link.name)}
    <div  class="button">
      <button class="button--click "on:click={() => goToUrl(link.url)}>{link.name}</button>
      <span class="button--icon"><i class={link.icon}></i></span>
    </div>
    {/each}
</main>

<style>
  h1 {
    margin: auto;
  }
  main {
    margin: auto;
    margin-top: 200px;
  }
  .button {
    display: flex;
    flex-direction: row-reverse;
    justify-content: left;
  }
  .button--icon {
    visibility: hidden;
    padding: 2px 5px 2px 5px;
  }
  .button--click {
    width: fit-content;
    padding: 2px 10px 2px 10px;
    border: 1px solid #213547;
    border-radius: 0;
    margin-bottom: 5px;
  }
  .button--click:hover {
    background-color: #213547;
    color: white;
    cursor: pointer;
  }
  .button--click:hover + .button--icon {
    visibility:visible !important;
  }
</style>
