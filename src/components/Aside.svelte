<script lang="ts">
  export let open: boolean = false
  export let sticky: boolean = true
</script>

<style>
  aside {
    width: 0;
    transform: translateX(calc(var(--sidebar-width) * -1));
    transition: all 0.2s;
    background-color: var(--secondary-light);
  }

  .open {
    width: var(--sidebar-width);
    transform: translateX(0);
  }

  .content {
    padding: 1rem;
  }

  .sticky {
    position: sticky;
    top: var(--header-height);
  }
</style>

<aside class:open>
  <div class="content" class:sticky>
    <h1>Aside Title</h1>
    <p>Aside</p>
  </div>
</aside>
