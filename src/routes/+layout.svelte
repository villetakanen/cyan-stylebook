<script lang="ts">
  function toggleGuides (event: Event) {
    const on = (event.target as HTMLInputElement).checked
    if (on) {
      document.querySelector('main')?.classList.add('withGuides')
    } else {
      document.querySelector('main')?.classList.remove('withGuides')
    }
  }
  </script>

<cyan-top-app-bar title="Cyan Elements Stylebook" menu role="banner">
  <cyan-nav-menu-button />
  <h2>Cyan Elements Stylebook</h2>
  <cyan-spacer />
  <cyan-lightmode-toggle />
</cyan-top-app-bar>
<nav id="tray">
  <a href="/">
    <cyan-nav-button text noun="stylebook">Introduction</cyan-nav-button>
  </a>
  <a href="/typography">
    <cyan-nav-button noun="font">Typography</cyan-nav-button>
  </a>
  <hr>
  <a href="/cyan-top-app-bar">
    <cyan-nav-button noun="page">cyan-top-app-bar</cyan-nav-button>
  </a>
  <cyan-toggle label="Visual Guides" on:change={toggleGuides} />
</nav>

<slot></slot>

<style lang="sass">
#tray
  position: fixed
  top: 72px
  left: 0
  display: flex
  flex-direction: column
  gap: 8px
  width: 220px
  padding-left: 16px
</style>