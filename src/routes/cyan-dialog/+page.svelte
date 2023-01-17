<script lang="ts">
	import type { CyanDialog } from "src/cyan-elements/src";


let rval = ''
const onclose = (e:Event) => {
  const rval = (e.target as CyanDialog).returnValue;
}

function openDialog() {
    const dialog = document.querySelector('cn-dialog') as CyanDialog;
    dialog.showModal()
}

</script>
<main class="bookLayout">
  <article class="Column small">
    <cyan-button
      noun="add"
      label="Open Dialog"
      on:keydown={openDialog}
      on:click={openDialog} />
  </article>
  <cn-dialog title="An Example Dialog, with very long and arduous title" on:close={onclose}>
    <cn-tabs tabs={[['test', 'Test'], ['test2', 'Test 2'], ['test3', 'Test 3 - Long Tab Name']]} active="test" />
    <p>Here is a dialog</p>
    <p>It has a title and a close button</p>
    <p>It can be closed by clicking the close button or by pressing the escape key</p>
    <cyan-button noun="close" on:click={onclose} on:keydown={onclose} />
    <cyan-lightmode-toggle />
  </cn-dialog>
</main>