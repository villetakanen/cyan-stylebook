<script lang="ts">
import AppBar from "$lib/AppBar.svelte";

let count = 4
function handleClick(e: CustomEvent) {
  count = e.detail
}
</script>



<AppBar />

<main class="bookLayout">
  <article class="Column">
    <h1>Cyan-love-button</h1>
    <p>Here is a cyan love button.</p>
    <cyan-love-button count={count} on:change={handleClick} />
  </article>
</main>