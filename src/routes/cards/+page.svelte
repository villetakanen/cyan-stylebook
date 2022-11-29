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
  <article class="Column medium">
    <cyan-card elevation="1" cover="/proprietary/images/example_1.jpeg">
      <h3 slot="title">With an Image</h3>
      <cyan-icon noun="card" slot="avatar" large dark/>
      <p class="downsized">This card has a cover image.</p>
    </cyan-card>
  </article>
  <article class="Column small" style="display:flex; flex-direction:column; gap: 8px">
    <cyan-card elevation="0">
      <h4 slot="title">Elevation 0</h4>
      <cyan-icon noun="mekanismi" slot="avatar" />
    </cyan-card>
    <cyan-card elevation="1">
      <h4 slot="title">Elevation 1</h4>
      <cyan-icon noun="ll" slot="avatar" />
    </cyan-card>
    <cyan-card elevation="2">
      <h4 slot="title">Elevation 2</h4>
      <cyan-icon noun="quick" slot="avatar" />
    </cyan-card>
    <cyan-card elevation="3">
      <h4 slot="title">Elevation 3 and a very long title</h4>
      <cyan-icon noun="dd" slot="avatar" />
    </cyan-card>
  </article>
</main>