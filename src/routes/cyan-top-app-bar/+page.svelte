<script lang="ts">

let menu = false;
let sticky = false;
let modal = false;

const toggleMenu = () => {
  menu = !menu;
};
const toggleModal = () => {
  modal = !modal;
};
const toggleSticky = () => {
  sticky = !sticky;
};
</script>

<main class="bookLayout">
  <article class="Column full">
    <h1>cyan-top-app-bar</h1>
    <p><cyan-code>{'<cyan-top-app-bar [sticky] [modal]>'}</cyan-code></p>
    <cyan-top-app-bar menu={menu} sticky={sticky} modal={modal}>
      <cyan-icon icon="fox" />
      <h2>An example App Bar</h2>
      <cyan-spacer />
      <cyan-button text noun="kebab" on:click={toggleMenu} on:keydown={toggleMenu} active={menu}/>
      <cyan-button text noun="check" on:click={toggleSticky} on:keydown={toggleSticky} active={modal}/>
      <cyan-button text noun="back" on:click={toggleModal} on:keydown={toggleModal} active={sticky}/>
    </cyan-top-app-bar>
    <p>... scroll ...</p>
    <p>... scroll ...</p>
    <p>... scroll ...</p>
    <p>... scroll ...</p>
    <p>... scroll ...</p>
    <p>... scroll ...</p>
    <p>... scroll ...</p>
    <p>... scroll ...</p>
    <p>... scroll ...</p>
    <p>... scroll ...</p>
    <p>... scroll ...</p>
    <p>... scroll ...</p>
    <p>... scroll ...</p>
    <p>... scroll ...</p>
    <p>... scroll ...</p>
    <p>... scroll ...</p>
  </article>
</main>