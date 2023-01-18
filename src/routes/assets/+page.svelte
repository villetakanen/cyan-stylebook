<main class="bookLayout">
  <article class="small Column">
    <cyan-card elevation="1">
      <h2 slot="title">Assets</h2>
      <cyan-icon noun="books" slot="avatar" />
      <p class="TypeCaption">Various Asset related components.</p>
    </cyan-card>
  </article>

  <article class="Column">
    <h3>Asset Tokens</h3>
    <p>
      The <cyan-code>&lt;cyan-asset-token&gt;</cyan-code> component is used to display
      icons for various asset types.
    </p>
    <section class="flex flex-wrap">
      <cn-asset-token
        type="image/webp"
        label="a WebP Image"
        preview="https://www.gstatic.com/webp/gallery/4.webp"
      />
      <cn-asset-token
        type="application/pdf"
        label="a PDF file"
      />
      <cyan-asset-token noun="audio" />
      <cyan-asset-token noun="pdf" />
      <cyan-asset-token noun="doc" />
      <cyan-asset-token noun="xls" />
      <cyan-asset-token noun="ppt" />
      <cyan-asset-token noun="zip" />
      <cyan-asset-token noun="other" />
    </section>
  </article>
</main>