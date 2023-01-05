<script lang="ts">
	import type { CyanToggle } from "src/cyan-elements/src";


let disabled = false
function setDisabled (e: Event) {
  disabled = (e.target as CyanToggle).checked
}
</script>

<main class="bookLayout">
  <article class="Column small">
    <cyan-card elevation="1" style="text-align: center">
      <cyan-icon noun="add-discussion" large/>
      <h3>Buttons</h3>
    </cyan-card>
  </article>
  <article class="Column">
    <h2>F.A.B.</h2>
    <section style="display: flex; flex-direction: column; gap: 8px">
      <cyan-fab noun="edit">Fabs!</cyan-fab>
      <cyan-fab noun="add" secondary>Secondary Fabs?</cyan-fab>
      <cyan-fab noun="delete" small>Small Fabs O_o</cyan-fab>
      <cyan-fab noun="spacer" small secondary>Secondary, with spacer</cyan-fab>
    </section>
  </article>
  <article class="small Column">
    <h3>Buttons</h3>
    <section class="fieldset">
      <cyan-toggle checked={disabled} on:change={setDisabled} label="Disables"/>
      <cyan-button disabled={disabled} label="Button"></cyan-button>
      <cyan-button disabled={disabled} secondary label="Secondary"></cyan-button>
      <cyan-button disabled={disabled} text label="Text"></cyan-button>
    </section>
  </article>
</main>