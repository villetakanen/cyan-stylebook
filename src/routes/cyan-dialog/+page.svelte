<script lang="ts">
let dialog = false;

const onkey = (e:KeyboardEvent) => {
  if (e.key === 'Enter') {
    dialog = true;
  }
};
const onclose = (e:Event) => {
  dialog = false;
};
</script>
<main class="bookLayout">
  <article class="Column small">
    <cyan-button
      noun="add"
      label="Open Dialog"
      on:keydown={onkey}
      on:click={() => {
        dialog = true;
      }} />
  </article>
  <cyan-dialog open={dialog} title="An Example Dialog, with very long and arduous title" on:close={onclose}>
    <p>Here is a dialog</p>
    <p>It has a title and a close button</p>
    <p>It can be closed by clicking the close button or by pressing the escape key</p>
    <cyan-button noun="close" on:click={onclose} on:keydown={onclose} />
    <cyan-lightmode-toggle />
  </cyan-dialog>
</main>