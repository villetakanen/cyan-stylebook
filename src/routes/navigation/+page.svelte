<script>
	import AppBar from "$lib/AppBar.svelte";
	import MenuButton from "$lib/MenuButton.svelte";
</script>

<AppBar />

<main class="bookLayout">
  <article class="Column medium">
	<h2>Navigation Bar/Tray Buttons</h2>
    <cyan-navigation-button noun="font" label="Typography" />
  </article>
  <MenuButton />
</main>