<script lang="ts">
  import Header from './Header.svelte'
  import Hamburger from './Hamburger.svelte'
  import Aside from './Aside.svelte'
  import Main from './Main.svelte'

  let asideOpen: boolean = false
  let asideWidth: string
</script>

<style>
  .app {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }
</style>

<div class="app" style="--aside-width: 20rem;">
  <Header />
  <Hamburger bind:checked={asideOpen} />
  <Aside open={asideOpen} bind:asideWidth />
  <Main offsetLeft={asideWidth} />
</div>
