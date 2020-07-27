<script>
  import { createEventDispatcher } from 'svelte'

  const dispatch = createEventDispatcher()
  let open = false

  $: dispatch('menuToggle', { menuOpen: open })
</script>

<style>
  input[type='checkbox'] {
    transition: all 0.2s;
    box-sizing: border-box;
    display: none;
  }

  .nav-icon {
    width: 2rem;
  }

  .nav-icon:after,
  .nav-icon:before,
  .nav-icon div {
    background-color: #fff;
    border-radius: 3px;
    content: '';
    display: block;
    height: 5px;
    margin: 7px 0;
    transition: all 0.1s ease-in-out;
  }

  .open.nav-icon:before {
    transform: translateY(12px) rotate(45deg);
  }

  .open.nav-icon:after {
    transform: translateY(-12px) rotate(-45deg);
  }

  .open.nav-icon div {
    transform: scale(0);
  }
</style>

<div>
  <input type="checkbox" bind:checked={open} id="openSidebarMenu" />
  <label for="openSidebarMenu" class="nav-icon" class:open>
    <div />
  </label>
</div>
