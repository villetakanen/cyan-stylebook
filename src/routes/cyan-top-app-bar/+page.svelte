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
    <cyan-top-app-bar menu={menu} sticky={sticky} modal={modal}>
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