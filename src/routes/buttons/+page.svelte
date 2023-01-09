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
    <h4>CSS Button Styles</h4>
    <p class="TypeBody2">Shadow DOM and ability to capsulate functionality - means 
      we need to re-implement lots of functionality offered by browsers for the standard
      html button element. Thus: providing a styling for the standard button is simpler
      to implement - and far more functionable, than using a Web Component to style a 
      _standard_ button.</p>
    <p class="TypeBody2">All of these styles except a a parent (likely <cyan-code>{'<body>'}</cyan-code>) with
      the class <cyan-code>{'.cyan'}</cyan-code></p>
      <section class="fieldset">
        <cyan-toggle checked={disabled} on:change={setDisabled} label="Disabled"/>
        <div>
          <button disabled={disabled}>Button</button>
          <button disabled={disabled}><cyan-icon noun="fox" small/></button>
          <button disabled={disabled}><cyan-icon noun="fox" small/><span>Button + Icon</span></button>
        </div>
        <div>
          <button disabled={disabled} class="secondary">Secondary</button>
          <button disabled={disabled} class="secondary"><cyan-icon noun="d20" small/></button>
          <button disabled={disabled} class="secondary"><cyan-icon noun="d20" small/><span>Text + Icon</span></button>
        </div>
        <div>
          <button disabled={disabled} class="text">Text</button>
          <button disabled={disabled} class="text"><cyan-icon noun="d20" small/></button>
          <button disabled={disabled} class="text"><cyan-icon noun="d20" small/><span>Text + Icon</span></button>
        </div>
      </section>
      <h4>Cyan-button</h4>
      <p class="TypeCaption"><i>the cyan-button</i> is a dev-time legacy element. By 1.0.0, this should be replaced with a regular button</p>
      <section class="fieldset">
        <cyan-toggle checked={disabled} on:change={setDisabled} label="Disabled"/>
        <cyan-button noun="icons" disabled={disabled} label="Button"></cyan-button>
        <cyan-button disabled={disabled} secondary label="Secondary"></cyan-button>
        <cyan-button disabled={disabled} text label="Text"></cyan-button>
      </section>
  </article>
</main>