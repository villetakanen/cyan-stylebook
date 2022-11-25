<script>
import AppBar from "$lib/AppBar.svelte"
import MenuButton from "$lib/MenuButton.svelte"
</script>

<AppBar />

<main class="bookLayout">
  <article class="Column medium">
	<h2>Navigation Bar/Tray Buttons</h2>
  <p>Navigation Bar and Tray use material -inspired buttons. These buttons should be enclosed in
    <cyan-code>{'<a></a>'}</cyan-code> tags</p>
    <cyan-toolbar>
      <cyan-navigation-button noun="font" label="Typography" />
      <cyan-navigation-button noun="mekanismi" />
    </cyan-toolbar>
  </article>
  <MenuButton />
</main>