<script>
  import Hamburger from './Hamburger.svelte'

  // your script goes here
</script>

<style>
  :global(.icon) {
    padding: 0.5rem;
  }

  header {
    position: sticky;
    top: 0;
    background-color: var(--primary-dark);
    color: var(--primary-light);
    display: flex;
    align-items: center;
    min-height: var(--header-height);
    padding: 0 1rem;
    z-index: 2;
  }

  .title {
    font-size: 1.5rem;
    vertical-align: middle;
    margin-left: 1rem;
  }
</style>

<header>
  <Hamburger on:hamburgerToggle />
  <div class="title">Header</div>
</header>
