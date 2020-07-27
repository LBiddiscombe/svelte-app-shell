<script lang="ts">
  import Header from './Header.svelte'
  import Aside from './Aside.svelte'
  import Main from './Main.svelte'

  let asideOpen: boolean = false

  function handleHamburger(event: any) {
    asideOpen = event.detail.open
  }
</script>

<style>
  .app {
    --primary-dark: #333;
    --primary-light: #fff;
    --secondary-dark: #555;
    --secondary-light: #eee;
    --accent: #fed024;
    --header-height: 4rem;
    --sidebar-width: 20rem;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }

  .content {
    display: flex;
    min-height: calc(100vh - var(--header-height));
  }
</style>

<div class="app">
  <Header on:hamburgerToggle={handleHamburger} />
  <div class="content">
    <Aside open={asideOpen} />
    <Main />
  </div>
</div>
