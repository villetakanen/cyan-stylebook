<script>
	import AppBar from "$lib/AppBar.svelte";
	import Column from "$lib/Column.svelte";
	import Controls from "$lib/Controls.svelte";
import Intro from "$lib/Intro.svelte";
	import MenuButton from "$lib/MenuButton.svelte";
</script>

<AppBar />

<main class="bookLayout">
  <Intro />
  <Column />
  <MenuButton />
</main>

<Controls />
