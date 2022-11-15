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
</div>

<style lang="sass">
#controls
  position: fixed
  bottom: 0
  right: 0
  padding: 1rem
  z-index: 1000
</style>