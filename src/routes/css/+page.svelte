<script lang="ts">
import CssVariableInfo from "$lib/CSSVariableInfo.svelte"
</script>

<main class="bookLayout">
  <article class="Column small">
    <cyan-card elevation="1">
      <h3>CSS Variables</h3>
      <p>These are the core variables used in the component library.</p>
      <p>Please apply the class <cyan-code>.cyan</cyan-code> to body to apply the variables</p>
    </cyan-card>
  </article>
  <article class="Column small">
    <h4>Layout</h4>
    <CssVariableInfo name="--cn-page-grid" />
    <CssVariableInfo name="--cn-margin" />
    <CssVariableInfo name="--cn-padding" />
    <CssVariableInfo name="--cn-gap-row" />
    <CssVariableInfo name="--cn-gap-column" />
    <CssVariableInfo name="--cn-gap-toolbar" />
  </article>
</main>