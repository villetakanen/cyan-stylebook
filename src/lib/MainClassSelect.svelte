<script lang="ts">
import type { CyanSelect } from "src/cyan-elements/src";


let options = [
  { label: '.bookLayout', value: 'bookLayout' },
  { label: '.emptyLayout', value: 'emptyLayout' },
  { label: '.dahsboardLayout', value: 'dashboardLayout'},
  { label: '.singleColumnLayout', value: 'singleColumnLayout' },
  { label: '.gridLayout', value: 'gridLayout' }
]
function changeMainClass (event: Event) {
  document.querySelector('main')?.classList.remove('bookLayout')
  document.querySelector('main')?.classList.remove('dashboardLayout')
  document.querySelector('main')?.classList.remove('singleColumnLayout')
  document.querySelector('main')?.classList.remove('gridLayout')

  const main = document.querySelector('main')
  const value = (event.target as CyanSelect).value

  document.querySelector('main')?.classList.add(value)
}
</script>

<form>
  <cyan-select options={options} label="<main> Layout class" on:change={changeMainClass} role="listbox"/>
</form>