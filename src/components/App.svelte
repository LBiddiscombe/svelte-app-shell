<script lang="ts">
  import MenuToggle from './MenuToggle.svelte'

  export let name: string

  let asideOpen: boolean

  function handleMenuToggle(event: any) {
    asideOpen = event.detail.menuOpen
  }
</script>

<style>
  .wrapper {
    display: grid;
    grid-template-columns: 1fr 4fr;
    grid-template-rows: auto 1fr;
    grid-column-gap: 0px;
    grid-row-gap: 0px;
    min-height: 100vh;
  }

  header {
    position: sticky;
    top: 0;
    grid-column: 1 / -1;
    background-color: var(--primary-dark);
    color: var(--primary-light);
    display: flex;
    min-height: 4rem;
    align-items: center;
    padding: 0 1rem;
    z-index: 2;
  }

  .content {
    grid-column: 1/-1;
    grid-row: 2;
    display: flex;
  }

  aside {
    width: 0;
    opacity: 0;
    visibility: hidden;
    transition: all 0.2s;
    background-color: var(--secondary-light);
  }

  .aside-content {
    position: sticky;
    top: 4rem;
    padding: 1rem;
  }

  .asideOpen {
    visibility: visible;
    opacity: 1;
    width: 30rem;
  }

  main {
    padding: 1rem;
    flex: 1;
  }

  :global(.icon) {
    padding: 0.5rem;
  }

  .title {
    font-size: 1.5rem;
    vertical-align: middle;
    margin-left: 1rem;
  }
</style>

<div class="wrapper">
  <header>
    <MenuToggle on:menuToggle={handleMenuToggle} />
    <div class="title">Header</div>
  </header>

  <div class="content">
    <aside class:asideOpen>
      <div class="aside-content">Aside</div>
    </aside>

    <main>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
      <p>Hello {name}</p>
    </main>
  </div>
</div>
