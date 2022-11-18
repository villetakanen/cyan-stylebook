<script lang="ts">
let open = false
function toggleMenu(e: CustomEvent) {
  const t = e.detail
  // console.log('toggleMenu', t.getAttribute('open'))
  open = t
}
</script>

<article class="Column">
  <h2>Nav</h2>
  <h3>Menu button</h3>
  <p>The Nav Menu Button is a <a href="#themedElementInfo">themed</a> button that opens a drawer. It supports setting the noun to match the current context.</p>
  <cyan-nav-menu-button open={open} on:change={toggleMenu} />
  <p>The button above thinks the drawer is <cyan-code>{ open ? 'open' : 'closed'}</cyan-code></p>
  <h3>Nav buttons</h3>
  <section class="card rise-a" style="display:flex; flex-direction:column; gap: 8px">
    <cyan-nav-button noun="page">Page</cyan-nav-button>
    <cyan-nav-button noun="mekanismi">Wiki</cyan-nav-button>
    <cyan-nav-button noun="fox">Home</cyan-nav-button>
    <hr>
    <cyan-nav-button>Button, with ridiculously long text - that eventually should be clipped with an ellipsis</cyan-nav-button>
    <cyan-nav-button compact>Button</cyan-nav-button>
    <cyan-nav-button compact>Button</cyan-nav-button>
  </section>
</article>