<template>
  <div class="header">
    <h1 class="header__title">Baralho</h1>
    <nav class="header__nav">
      <button class="header__nav__button">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path d="M24 6h-24v-4h24v4zm0 4h-24v4h24v-4zm0 8h-24v4h24v-4z"/></svg>
      </button>
      <ul class="header__nav__items">
        <li class="header__nav__items__item">
          <a href="http://" target="_blank" rel="noopener noreferrer"></a>
        </li>
        <li class="header__nav__items__item">
          <a href="http://">Teste 2</a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  
}
</script>

<style lang="scss" scoped>
.header {
  top: 0;
  width: 100%;
  background-color: #1d1227;
  display: flex;
  justify-content: space-between;
  align-items: center;

  &__title {
    font-weight: 400;
    margin: 0.5rem 1rem;
    font-size: 2rem;
    text-transform: uppercase;
    color: white;
    font-family: 'Patua One', cursive;
  }

  &__nav {
    margin: 0.5rem 1rem;

    &__button {
      background-color: transparent;
      border: none;
      fill: whitesmoke;
    }

    &__items {
      display: none;
    }
  }
}
</style>