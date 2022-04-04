<template>
  <div class="footer">
    <button class="footer__button footer__button--new-card">Tirar carta</button>
    <button class="footer__button footer__button--start-over">
      <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path d="M13.5 2c-5.621 0-10.211 4.443-10.475 10h-3.025l5 6.625 5-6.625h-2.975c.257-3.351 3.06-6 6.475-6 3.584 0 6.5 2.916 6.5 6.5s-2.916 6.5-6.5 6.5c-1.863 0-3.542-.793-4.728-2.053l-2.427 3.216c1.877 1.754 4.389 2.837 7.155 2.837 5.79 0 10.5-4.71 10.5-10.5s-4.71-10.5-10.5-10.5z"/></svg>
    </button>
  </div>
</template>

<script>
export default {
  
}
</script>

<style lang="scss" scoped>
.footer {
  display: grid;
  grid-template-columns: 1fr auto;
  position: fixed;
  bottom: 0;
  left: 0;
  padding: 0.5rem 0.5rem 1.5rem 0.5rem;
  width: calc(100% - 1rem);
  /* From https://css.glass */
  background: rgba($color: white, $alpha: 0.4);
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  /* backdrop-filter: blur(2.9px);
  -webkit-backdrop-filter: blur(2.9px); */

  &__button {
    font-size: 1.5rem;
    border-radius: 0.5rem;
    padding: 0.5rem;
    display: flex;
    align-items: center;
    justify-content: center;
    border: none;
    font-family: 'Patua One', cursive;
    text-transform: uppercase;
    color: whitesmoke;

    &--new-card {
      background-color: rgba($color: rgb(29, 18, 39), $alpha: 0.8);
      box-shadow: 0 4px 30px rgba(0, 0, 0, 0.4);
    }

    &--start-over {
      border-color: transparent;
      background-color: transparent;
      border-radius: 9999px;
      fill: whitesmoke;
    }
  }
}
</style>