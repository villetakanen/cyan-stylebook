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
  <a href="/cards">
    <cyan-navigation-button noun="card" label="Cards"></cyan-navigation-button>
  </a>
  <a href="/inputs">
    <cyan-navigation-button noun="page" label="Inputs"></cyan-navigation-button>
  </a>
  <cyan-spacer></cyan-spacer>
  <cyan-lightmode-toggle />
</cyan-navigation-rail>

<div style="margin-left: 80px">

<cyan-top-app-bar title="Cyan Elements Stylebook" menu role="banner">
  <h2>Cyan Elements Stylebook</h2>
  <cyan-spacer />
  <cyan-lightmode-toggle />
</cyan-top-app-bar>

<slot></slot>

</div>

<cyan-navigation-tray id="tray" open={showTray}>
  <a href="/">
    <cyan-nav-button text noun="stylebook">Introduction</cyan-nav-button>
  </a>
  <a href="/css">
    <cyan-nav-button noun="d20">CSS Variables</cyan-nav-button>
  </a>
  <a href="/css/class">
    <cyan-nav-button noun="d20">CSS Classes</cyan-nav-button>
  </a>
  <a href="/core-components">
    <cyan-nav-button noun="code">HTML Components</cyan-nav-button>
  </a>
  <a href="/typography">
    <cyan-nav-button noun="font">Typography</cyan-nav-button>
  </a>
  <a href="/iconography">
    <cyan-nav-button noun="d12">Iconography</cyan-nav-button>
  </a>
  <a href="/navigation">
    <cyan-nav-button noun="arrow-right">Navigation</cyan-nav-button>
  </a>
  <a href="/buttons">
    <cyan-nav-button noun="add-discussion">Buttons</cyan-nav-button>
  </a>
  <hr>
  <a href="/cyan-top-app-bar">
    <cyan-nav-button noun="page">cyan-top-app-bar</cyan-nav-button>
  </a>
  <a href="/cyan-toolbar">
    <cyan-nav-button noun="tools">cyan-toolbar</cyan-nav-button>
  </a>
  <a href="/cyan-dialog">
    <cyan-nav-button noun="page">cyan-dialog</cyan-nav-button>
  </a>
  <a href="/cyan-navigation-button">
    <cyan-nav-button noun="page">cyan-navigation-button</cyan-nav-button>
  </a>
  <p style="padding: 12px">
    <cyan-toggle label="Visual Guides" on:change={toggleGuides} />
  </p>
</cyan-navigation-tray>

<!--style lang="sass">
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
</style-->