<script lang="ts">
	import Controls from "./Controls.svelte";

let isMenuOpen = false;

function toggleMenu(e: CustomEvent) {
  isMenuOpen = !!e.detail;
}
</script>

<cyan-toolbar large style="padding: 8px" sticky>
  <cyan-nav-menu-button
    open={isMenuOpen}
    on:change={toggleMenu}
  ></cyan-nav-menu-button>
  <cyan-spacer />
  <cyan-lightmode-toggle />
</cyan-toolbar>

{#if isMenuOpen }
<div class="drawer rise-d">
  <Controls />
</div>
{/if}

<style lang="sass">
cyan-nav-menu-button
  z-index: 100000
  transition: transform 0.2s ease-in-out
  &[open]
    transform: translateX(194px)
.drawer
  position: fixed
  top: 0
  left: 0
  width: 256px
  height: 100vh
  z-index: 10000
  display: flex
  flex-direction: column
  justify-content: top
  align-items: left
  transition: opacity 0.2s ease-in-out
  box-sizing: border-box
  padding: 8px 16px
  padding-top: 72px
  border-radius: 0 8px 8px 0
</style>