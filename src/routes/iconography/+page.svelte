<script lang="ts">
import AppBar from "$lib/AppBar.svelte"
import nounsFile from '../../cyan-elements/public/proprietary/icons/nouns.json'
import type { CyanSelect } from "src/cyan-elements/src"

const nouns = nounsFile as Record<string, string>

const nounOptions = Object.keys(nouns).map(noun => ({ value: noun, label: noun }))
let selectedNoun = nounOptions[14].value

function selectNoun (event: Event) {
  selectedNoun = (event.target as CyanSelect).value
}
</script>
        
<AppBar />

<main class="bookLayout">
  <article class="Column">
    <h1>Iconography</h1>
    <p>Cyan provides a set of light and dark <i>nouns</i>, that can be used to communicate app functionality.</p>
    <p>The <cyan-code>{'<cyan-icon noun=[noun] [xsmall|small|large|xlarge] [dark|light]>'}</cyan-code> -element provides 
      a handy way to use and size the icons within an app.</p>

    <section>
      <h3>Sizing</h3>
      <cyan-select value={selectedNoun} options={nounOptions} on:change={selectNoun} />
      <div style="display:flex; gap: 8px; flex-wrap:wrap; justify-content: space-between; align-items: center">
        <div style="text-align: center">
          <cyan-icon noun={selectedNoun} xsmall />
          <p class="TypeCaption">xsmall <br>16px</p>
        </div>
        <div style="text-align: center">
          <cyan-icon noun={selectedNoun} small />
          <p class="TypeCaption">small <br>24px</p>
        </div>
        <div style="text-align: center">
          <cyan-icon noun={selectedNoun} />
          <p class="TypeCaption">(medium) <br>36px</p>
        </div>
        <div style="text-align: center">
          <cyan-icon noun={selectedNoun} large />
          <p class="TypeCaption">large <br>72px</p>
        </div>
        <div style="text-align: center">
          <cyan-icon noun={selectedNoun} xlarge />
          <p class="TypeCaption">large <br>128px</p>
        </div>
      </div>
    </section>

    <section>
      <h3>Available nouns</h3>
      <div class="icongrid">
        {#each nounOptions as noun}
          <div style="text-align: center" class="iconcell">
            <cyan-icon noun={noun.value} />
            <p class="TypeCaption">{noun.label}</p>
          </div>
        {/each}
      </div>
    </section>
  </article>
</main>

<style lang="sass">
.icongrid
  display: flex
  flex-wrap: wrap
  gap: 8px
  .iconcell
    overflow: hidden
    width: 20%
</style>