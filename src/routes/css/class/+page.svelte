<main class="bookLayout">
  <article class="small Column">
    <cyan-icon noun="font" large/>
    <h3>CSS Atomics</h3>
    <p>
      Cyan Elements provides a set of CSS classes that can be used to style
      elements. These classes are based on the CSS variables defined in the
      <a href="/css">CSS Variables</a> section.
    </p>
  </article>
  <article class="small Column">
    <h3>Containers</h3>
    <p><cyan-code>flex</cyan-code></p>
    <p class="typeCaption">Basic flexbox setup</p>
    <p><cyan-code>flex-column</cyan-code></p>
    <p class="typeCaption">Basic flexbox extension for flex-direction: column. Use with <cyan-code>flex</cyan-code></p>
  </article>

  <article class="small Column">
    <h3>Text</h3>
    <p><cyan-code>underscore</cyan-code></p>
    <h3 class="underscore downscaled">h3 with underscore</h3>
    <h4 class="underscore downscaled">h4 with underscore</h4>
  </article>

  <article class="Column small">
    <h3>Forms</h3>
    <p><cyan-code>fieldset</cyan-code></p>
    <section class="fieldset">
      <cyan-card>aaa</cyan-card>
      <cyan-card>bbb</cyan-card>
      <cyan-card>ccc</cyan-card>
    </section>
  </article>

  <article class="small Column">
    <h3>UX</h3>
    <p class="hoverable clickable">This paragraph is <cyan-code>.hoverable</cyan-code> and
      <cyan-code>.clickable</cyan-code>.</p>
    <ul class="hoverable">
      <li class="clickable">This list is  <cyan-code>.hoverable</cyan-code>, but only the 
        first item is <cyan-code>.clickable</cyan-code></li>
      <li>This, second item, is not clickable.</li>
    </ul>
  </article>
</main>