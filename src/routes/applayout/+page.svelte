<script lang="ts">
	import AppLayoutArticle from "./appLayoutArticle.svelte";

  
</script>
<div class="AppLayout">
  <main class="bookLayout">
    <article class="small Column">
      <cyan-card>
        <h2 slot="title" class="downscaled">App Layout</h2>
        <cyan-icon slot="avatar" noun="font"></cyan-icon>
        <p class="TypeBody2">Cyan comes with a set of app-layout classes and elements - to build a 
            Material design inspired SPA -skeleton.</p>
      </cyan-card>
    </article>
    <AppLayoutArticle />
  </main>
</div>
