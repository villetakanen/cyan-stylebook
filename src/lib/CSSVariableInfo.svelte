<script lang="ts">
import { onMount } from "svelte";

export let name = ''

let variable = ''

let component: HTMLElement

onMount(() => {
  variable = window.getComputedStyle(component).getPropertyValue(name)
})
</script>

<div class="CSSVariableInfo" bind:this={component}>
  <cyan-code>{ name }</cyan-code>
  <span class="value">{ variable }</span>
</div>

<style lang="sass">
.CSSVariableInfo
  width: 100%
  display: flex
  justify-content: space-between
  align-items: center
  height: var(--cn-page-grid)
  margin: var(--cn-margin) 0
  .value
    font-family: 'roboto mono', monospace
    color: var(--chroma-secondary-h)
    background-color: var(--chroma-primary-b)
    padding: 0 8px
    border-radius: 4px
</style>
