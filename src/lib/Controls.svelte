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

<div id="controls">
  <cyan-toggle label="Visual Guides" on:change={toggleGuides} />
  <a href="/">
    <cyan-nav-button noun="fox">Home</cyan-nav-button>
  </a>
  <a href="/intro">
    <cyan-nav-button>Intro</cyan-nav-button>
  </a> 
  <a href="/navigation">
    <cyan-nav-button>Navigation (and by the way, here is a really long text, that should clip></cyan-nav-button>
  </a>
  <a href="/cyan-love-button">
    <cyan-nav-button noun="button">Cyan Love Button</cyan-nav-button>
  </a>
  <a href="/cyan-loader">
    <cyan-nav-button noun="loader">Cyan Loader</cyan-nav-button>
  </a>
  <p>aaa</p>
  <cyan-nav-button compact>Button</cyan-nav-button>
  <cyan-nav-button compact>Button</cyan-nav-button>
</div>

<style lang="sass">
#controls
  display: flex
  flex-direction: column
  gap: 8px
</style>