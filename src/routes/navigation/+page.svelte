<script lang="ts">
import MenuButton from "$lib/MenuButton.svelte"
import type { CyanTabs } from "src/cyan-elements/src";

const tabs = [
  ['test', 'Test'],
  ['test2', 'Test 2'],
  ['test3', 'Test 3 - Long Tab Name']
]

let activeTab = 'test'
let test = 'test'

function changeTab(e: Event) {
  const tabElement = e.target as CyanTabs
  const a = tabElement.active
  console.log(a)
  test = a
  activeTab = a
}
</script>

<main class="bookLayout">
  <!-- Tabs! -->
  <article class="Column">
    <h4>Tabs</h4>
    <cn-tabs tabs={tabs} active={activeTab} on:change={changeTab}></cn-tabs>
    <p>Active tab is <cyan-code>{activeTab}</cyan-code> {test}</p>
  </article>

  <article class="Column medium">
	<h2>Navigation Bar/Tray Buttons</h2>
  <p>Navigation Bar and Tray use material -inspired buttons. These buttons should be enclosed in
    <cyan-code>{'<a></a>'}</cyan-code> tags</p>
    <cyan-toolbar>
      <cyan-navigation-button noun="font" label="Typography" />
      <cyan-navigation-button noun="mekanismi" />
    </cyan-toolbar>
  </article>
  <MenuButton />
</main>