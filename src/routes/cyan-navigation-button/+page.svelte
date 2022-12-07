<script lang="ts">
import nounsFile from '../../lib/nouns.json'
import type { CyanSelect, CyanTextfield, CyanToggle } from "src/cyan-elements/src"


// Noun for the button
const nouns = nounsFile as Record<string, string>

const nounOptions = Object.keys(nouns).map(noun => ({ value: noun, label: noun }))
let selectedNoun = nounOptions[17].value

function selectNoun (event: Event) {
  selectedNoun = (event.target as CyanSelect).value
}

let active = false
function setActive (e: Event) {
  active = (e.target as CyanToggle).checked
}

let notification = '9+'
function setNotification (e: Event) {
  notification = (e.target as CyanTextfield).value
}

</script>

<main class="bookLayout">
  <article class="Column">
    <h3 class="downscaled">cyan-navigation-button</h3>
    <form>
      <cyan-toolbar>
        <cyan-select
          style="flex-grow: 1"
          value={selectedNoun}
          options={nounOptions}
          on:change={selectNoun}
          label="Select noun for icon and label"/>
        <cyan-toggle checked={active} on:change={setActive} label="Set Active"/>
      </cyan-toolbar>
      <cyan-toolbar>
        <cyan-textfield label="Notification" value={notification} on:change={setNotification}/>
      </cyan-toolbar>
    </form>
    <cyan-navigation-button noun={selectedNoun} active={active} notification={notification}/>
    <cyan-navigation-button noun={selectedNoun} label={selectedNoun} active={active} notification={notification} />
  </article>
</main>