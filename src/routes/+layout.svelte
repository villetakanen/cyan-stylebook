<script lang="ts">
import type { CyanNavMenuButton } from "src/cyan-elements/src";

let showTray = false

function toggleMenu (event: Event) {
  showTray = (event.target as CyanNavMenuButton).open
}

function toggleGuides (event: Event) {
  const on = (event.target as HTMLInputElement).checked
  if (on) {
    document.querySelector('main')?.classList.add('withGuides')
  } else {
    document.querySelector('main')?.classList.remove('withGuides')
  }
}
</script>

<cyan-navigation-rail>
  <cyan-nav-menu-button on:change={toggleMenu}/>
  <a href="/">
    <cyan-navigation-button noun="stylebook" label="Intro"></cyan-navigation-button>
  </a>
  <a href="/typography">
    <cyan-navigation-button noun="font" label="Typo"></cyan-navigation-button>
  </a>
  <cyan-spacer></cyan-spacer>
  <cyan-lightmode-toggle />
</cyan-navigation-rail>

<div style="margin-left: 96px">

<cyan-top-app-bar title="Cyan Elements Stylebook" menu role="banner">
  <h2>Cyan Elements Stylebook</h2>
  <cyan-spacer />
  <cyan-lightmode-toggle />
</cyan-top-app-bar>

<slot></slot>

</div>

<nav id="tray" class:hide={!showTray} class="dark">
  <a href="/">
    <cyan-nav-button text noun="stylebook">Introduction</cyan-nav-button>
  </a>
  <a href="/typography">
    <cyan-nav-button noun="font">Typography</cyan-nav-button>
  </a>
  <a href="/iconography">
    <cyan-nav-button noun="d12">Iconography</cyan-nav-button>
  </a>
  <a href="/navigation">
    <cyan-nav-button noun="arrow-right">Navigation</cyan-nav-button>
  <hr>
  <a href="/cyan-top-app-bar">
    <cyan-nav-button noun="page">cyan-top-app-bar</cyan-nav-button>
  </a>
  <cyan-spacer />
  <cyan-toggle label="Visual Guides" on:change={toggleGuides} />
</nav>

<style lang="sass">
#tray
  position: fixed
  top: 72px
  left: 0
  display: flex
  flex-direction: column
  gap: 8px
  width: calc(220px + 2 * 16px)
  transition: transform 0.2s ease-in-out
  background-color: var(--chroma-secondary-c)
  height: calc(100vh - 80px)
  padding: 16px
  border-radius: 0 16px 16px 0
  box-sizing: border-box
  padding-bottom: 24px
  &.hide
    transform: translateX(-244px)
</style>