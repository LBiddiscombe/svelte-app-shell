<script lang="ts">
  import Icon from 'svelte-awesome'
  import { faHome, faTh, faAngleDoubleLeft, faAngleDoubleRight } from '@fortawesome/free-solid-svg-icons'

  export let open: boolean = false
  export let asideWidth: string = '20rem'

  let collapsed = false
  let collapseIcon

  $: {
    collapseIcon = collapsed ? faAngleDoubleRight : faAngleDoubleLeft
    asideWidth = open ? (collapsed ? '4rem' : '20rem') : '0'
  }
</script>

<style>
  aside {
    position: fixed;
    top: 0;
    left: 0;
    height: calc(100vh - var(--header-height));
    display: flex;
    flex-direction: column;
    padding-top: var(--header-height);
    transform: translateX(calc(var(--aside-width) * -1));
    transition: all 0.2s;
    background-color: var(--secondary-dark);
    background: linear-gradient(
      to right,
      var(--secondary-dark) 0,
      var(--secondary-dark) 4rem,
      var(--secondary-light) 4rem
    );
  }

  .open {
    width: var(--aside-width);
    transform: translateX(0);
  }

  .spacer {
    flex-grow: 1;
  }

  button {
    border: 0;
    background-color: transparent;
    padding: 8;
    margin: 0;
  }

  .item {
    display: flex;
    align-items: center;
    color: var(--primary-light);
    text-decoration: none;
    width: 100%;
    padding: 0.5rem;
    padding-right: 0;
  }

  .item:hover {
    background-color: rgba(255, 255, 255, 0.3);
    transition: 0.3s;
    transition-property: background-color;
  }

  .item span {
    padding-left: 1rem;
    justify-self: left;
    color: var(--secondary-dark);
  }
</style>

<aside class:open style={open && collapsed ? 'width: 4rem;' : open ? 'width: var(--aside-width)' : ''}>
  <button class="item" on:click={() => (collapsed = !collapsed)}>
    <Icon data={collapseIcon} scale="2" class="icon" />

  </button>
  <a href="/" class="item">
    <Icon data={faHome} scale="2" class="icon" />
    <span style={collapsed ? 'display: none' : ''}>Home</span>
  </a>
  <a href="/crossfade" class="item">
    <Icon data={faTh} scale="2" class="icon" />
    <span style={collapsed ? 'display: none' : ''}>Crossfade Demo</span>
  </a>
  <div class="spacer" />

</aside>
