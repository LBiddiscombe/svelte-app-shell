<script lang="ts">

</script>

<style>
  :global(.icon) {
    padding: 0.5rem;
  }

  header {
    position: fixed;
    top: 0;
    width: 100%;
    background-color: var(--primary-dark);
    color: var(--primary-light);
    display: flex;
    align-items: center;
    min-height: var(--header-height);
    padding-left: 4rem;
    z-index: 2;
    box-shadow: rgba(0, 0, 0, 0.14) 0 4px 5px 0, rgba(0, 0, 0, 0.12) 0 1px 10px 0, rgba(0, 0, 0, 0.3) 0 2px 4px -1px;
  }

  .title {
    font-size: 1.5rem;
    vertical-align: middle;
    margin-left: 1rem;
  }
</style>

<header>
  <div class="title">Header</div>
</header>
