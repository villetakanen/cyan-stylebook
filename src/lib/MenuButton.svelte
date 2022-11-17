<script lang="ts">
let open = false
function toggleMenu(e: CustomEvent) {
  const t = e.detail
  // console.log('toggleMenu', t.getAttribute('open'))
  open = t
}
</script>

<article class="Column">
  <h2>Menu Button</h2>
  { open }
  <cyan-nav-menu-button open={open} on:change={toggleMenu} />
</article>