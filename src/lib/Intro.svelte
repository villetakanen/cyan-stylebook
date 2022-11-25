<script lang="ts">
	import type { CyanSelect } from "src/cyan-elements/src";


let options = [
  { label: '.bookLayout', value: 'bookLayout' },
  { label: '.emptyLayout', value: 'emptyLayout' },
  { label: '.dahsboardLayout', value: 'dashboardLayout'},
  { label: '.singleColumnLayout', value: 'singleColumnLayout' }
]
function changeMainClass (event: Event) {
  document.querySelector('main')?.classList.remove('bookLayout')
  document.querySelector('main')?.classList.remove('dashboardLayout')
  document.querySelector('main')?.classList.remove('singleColumnLayout')

  const main = document.querySelector('main')
  const value = (event.target as CyanSelect).value

  document.querySelector('main')?.classList.add(value)
}
</script>

<article class="Column large">
  <h2>Cyan Elements Stylebook</h2>
  <p>This <strong>SvelteKit App</strong> acts as a kind of a Diary for the UX and UI design for the 
    cyan-elements. Additionally, it is a very convinient way to test and document usage of UX/UI 
    practices, tooling, components, and styles in the codebase.</p>
  <h3>Main area layout</h3>
  <p>Cyan Elements contains 3 layout models for the <cyan-code>{'<main>'}</cyan-code> area of a page. 
    Use the select below to swap between the modes.</p>
  <cyan-toolbar>
    <cyan-icon noun="page" />
    <cyan-select options={options} label="<main> Layout class" on:change={changeMainClass}/>
    <cyan-spacer />
  </cyan-toolbar>
  <table>
    <thead><tr><th>Class</th><th>Usage</th></tr></thead>
    <tbody>
      <tr>
        <td>
          <cyan-code>singleColumnLayout</cyan-code>
        </td><td>A simple layout with a single, centered column of text.</td></tr>
      <tr>
        <td>
            <cyan-code>dashboardLayout</cyan-code></td><td>A layout for dashboards. Arranges sections into rows of 3 items for desktop and tablet. (on mobile, acts like the <span class="code">singleColumnLayout</span>)</td></tr>
      <tr><td class="lowEmphasis" style="text-decoration: line-through;"><span class="code">withSideBarLayout</span></td><td class="lowEmphasis" style="text-decoration: line-through;"> A layout for wiki and game pages, with a site specific sidebar. </td></tr>
      <tr>
        <td><span class="code">emptyLayout</span></td>
        <td>A Naive layout that just expects the <cyan-code>Column</cyan-code>s to size themselves through CSS (or automatically by the rendering engine)</td>
      </tr>
      <tr>
        <td>
            <cyan-code>bookLayout</cyan-code></td><td>A layout with 2 sized columns. use class <span class="code">double</span> to get 2 columnns wide <span class="code">Column</span></td></tr>
    </tbody>
  </table>
</article>