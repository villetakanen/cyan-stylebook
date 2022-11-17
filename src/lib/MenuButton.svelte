<script lang="ts">
let open = false
function toggleMenu(e: CustomEvent) {
  const t = e.detail
  // console.log('toggleMenu', t.getAttribute('open'))
  open = t
}
</script>

<article class="Column">
  <h2>Nav Menu Button</h2>
  <p>The Nav Menu Button is a <a href="#themedElementInfo">themed</a> button that opens a drawer. It supports setting the noun to match the current context.</p>
  <cyan-nav-menu-button open={open} on:change={toggleMenu} />
  <p>The button above thinks the drawer is <cyan-code>{ open ? 'open' : 'closed'}</cyan-code></p>
</article>