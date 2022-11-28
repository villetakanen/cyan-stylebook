<main class="bookLayout">
  <article class="Column small">
    <cyan-card elevation="0">
      <h3 slot="title">Cards</h3>
      <cyan-icon noun="card" slot="avatar" />
      <p class="downsized">Cards are used as listings and call-to-actions, as a link to actual views of the entry.</p>
      <p class="downsized">A <cyan-code>{ '<cyan-card [cover=URL] elevation=[0...9]> '}</cyan-code> has three <i>slots</i>:
        <cyan-code>title</cyan-code>
        <cyan-code>avatar</cyan-code>, 
        and the default slot.</p>
    </cyan-card>
  </article>
  <article class="Column small">
    <cyan-card elevation="1">
      <h4 slot="title">Elevation 1</h4>
      <cyan-icon noun="ll" slot="avatar" />
    </cyan-card>
</main>