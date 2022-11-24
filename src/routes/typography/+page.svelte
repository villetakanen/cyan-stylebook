<main class="bookLayout">
  <article class="Column">
    <h2>Type Color</h2>
    <section>
      <h3>Paragraphs</h3>
      <p>This is a plain paragraph. The font family is <cyan-code>Cabin</cyan-code> and text-is either white, 
        or black, with opacity 0.87 and 0.74, respectively.</p>
      <p class="TypeBody2">This is a paragraph with the style <cyan-code>TypeBody2</cyan-code>, which should make the text a bit smaller.</p>
      <h4>Low emphasis</h4>
      <p class="lowEmphasis">This paragraph has the "atomic" style <cyan-code>lowEmphahis</cyan-code>, and should have low emphasis, and thus opacity of 0.60</p>
      <p class="TypeBody2 lowEmphasis">And the same, in the smaller text size</p>
      <h4>Disabled</h4>
      <p disabled>This paragraph is <cyan-code>disabled</cyan-code>, and should have, and thus opacity of 0.38</p>
    </section>
  </article>

  <article class="Column full">
    <h2>Column width</h2>
    <p class="TypeBody2 lowEmphasis">The width of text elements is bounded by artificial <cyan-code>ch</cyan-code>.</p>

    <div class="widthExamples">
      <div class="wd1 TypeBody2">
        This div is 67ch wide
      </div>
      <div class="wd2 TypeBody2">
        This div is 42ch wide (golden ratio from 67ch)
      </div>
      <div class="wd3 TypeBody2">
        This div is 26ch wide (golden ratio from 42ch)
      </div>
    </div>
    <p>The three "book-sized" paragraphs lend us to following measurements:</p>
    <ul>
      <li>67ch is roughly 700 px (in 4px increments)</li>
      <li>42ch is roughly 440 px (in 4px increments)</li>
      <li>26ch is roughly 272 px (in 4px increments)</li>
    </ul>
    <p>If a container is wider than 700px, a paragraph should have 2 columns.</p>
  </article>
</main>

<style>
.widthExamples {
  overflow: visible;
}
.wd1 {
  background-color: var(--chroma-primary-c);
  width: 67ch;
}
.wd2 {
  background-color: var(--chroma-primary-d);
  width: 42ch;
}
.wd3 {
  background-color: var(--chroma-primary-e);
  width: 26ch;
  overflow: hidden;
  height: 24px;
  text-overflow: ellipsis;
  white-space: nowrap;
}
</style>