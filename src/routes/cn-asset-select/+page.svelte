<script lang="ts">
	import type { CyanAssetSelect } from "src/cyan-elements/src";


let selected = 'a';
function handleSelect(e: Event) {
  selected = (e.target as CyanAssetSelect).selected
}
</script>

<main class="bookLayout">
  <article class="Column large">
    <h3>cn-asset-select</h3>
    <p>Selected is <cyan-code>{selected}</cyan-code></p>
    <cn-asset-select selected="a" on:change={handleSelect}>
      <cn-asset-option 
        selected
        value="a"
        preview="https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885__340.jpg"
      >
        aaa
      </cn-asset-option>
      <cn-asset-option
        value="b"
        preview="https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885__340.jpg">bbb</cn-asset-option>
      <cn-asset-option
        preview="https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885__340.jpg"
      >aaa</cn-asset-option>
      <cn-asset-option
        preview="https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885__340.jpg"
      >aaa</cn-asset-option>

      <cn-asset-option
        preview="https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885__340.jpg"
        value="c"
        >C is the option!</cn-asset-option>

      <cn-asset-option
        preview="https://cdn.pixabay.com/photo/2015/04/23/22/00/tree-736885__340.jpg"
        value="d"
        >D is the option!</cn-asset-option>
    
    </cn-asset-select>
  </article>
</main>