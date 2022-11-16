<script>
	import AppBar from "$lib/AppBar.svelte";
	import Column from "$lib/Column.svelte";
	import Controls from "$lib/Controls.svelte";
import Intro from "$lib/Intro.svelte";
</script>

<AppBar />

<main class="bookLayout">
  <Intro />
  <Column />
</main>

<Controls />
