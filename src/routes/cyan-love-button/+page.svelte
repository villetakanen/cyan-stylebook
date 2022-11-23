<script lang="ts">
import AppBar from "$lib/AppBar.svelte";
import type { CyanLoveButton } from "src/cyan-elements/src";

let count = 4
function handleClick(e: CustomEvent) {
  count = (e.target as CyanLoveButton).count
}
</script>

<AppBar />

<main class="bookLayout">
  <article class="Column">
    <h1>Cyan-love-button</h1>
    <p>Here is a cyan love button with {count} likes.</p>
    <cyan-toolbar small>
      <cyan-spacer></cyan-spacer>
      <cyan-love-button count={count} on:change={handleClick} />
    </cyan-toolbar>
  </article>
</main>