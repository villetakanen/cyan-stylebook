<script lang="ts">
import type { CyanSelect } from "src/cyan-elements/src";
import MainClassSelect from "./MainClassSelect.svelte";

let elevation = 0

const elevationOptions = [
  { label: '1', value: '0'},
  { label: '2', value: '1'},
  { label: '3', value: '2'},
  { label: '4', value: '3'},
]

function setCardElevation(e: Event) {
  const target = e.target as CyanSelect;
  elevation = parseInt(target.value);
}

</script>

<article class="Column">
  <h2>Form Section</h2>
  <p>We provide a responsive styling class <cyan-code>.fieldset</cyan-code> for form sections. This class allows us
    to simply smash all sorts of inputs and cyan-input fields to a semi coherent stucture in a form.</p>

  <cyan-select options={elevationOptions} on:change={setCardElevation}/>

  <p>{ elevation }</p>

  <cyan-card elevation={elevation}>
    <h3>Example</h3>
    <section class="fieldset">
      <cyan-textfield label="First Name" placeholder="First Name" />
      <cyan-textfield label="Last Name" placeholder="Last Name" />
      <cyan-textfield label="Email" placeholder="Email" />
      <MainClassSelect />
      <cyan-toolbar>
        <cyan-spacer />
        <cyan-button text label="Cancel"></cyan-button>
        <cyan-button label="Submit"></cyan-button>
      </cyan-toolbar>
    </section>
    <section class="fieldset">
      <cyan-toolbar>
        <cyan-textfield label="First Name" placeholder="First Name" />
        <cyan-textfield label="Last Name" placeholder="Last Name" style="flex-grow:1" />
      </cyan-toolbar>
    </section>
  </cyan-card>
</article>