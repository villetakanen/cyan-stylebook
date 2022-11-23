<script lang="ts">
import AppBar from "$lib/AppBar.svelte";    
</script>
    
<AppBar />
    
<main class="bookLayout">
  <article class="Column cut">
    <h1>Cyan-loader</h1>
    <p>A <cyan-code>{'<cyan-container [large|inline]>'}</cyan-code> component provides light and dark mode compatible loading animations.</p>
    <section class="card rise-a" style="text-align:center">
      <cyan-loader></cyan-loader>
    </section>
    <h3>Inline</h3>
    <p>An inline loader <cyan-loader inline></cyan-loader> can be placed, inline</p>
    <h4>Large</h4>
    <cyan-loader large />
  </article>
 </main>