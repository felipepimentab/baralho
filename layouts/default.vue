<template>
  <div id="baralho">
    <header>
      <AppHeader />
    </header>
    <main>
      <Nuxt />
    </main>
    <footer>
      <AppFooter />
    </footer>
  </div>
</template>

<style lang="scss">
html, body, #__nuxt, #__layout, #baralho {
  position: absolute;
  top: 0;
  left: 0;
  height: 100vh;
  width: 100vw;
  overflow: hidden;
  font-family: 'Rubik', sans-serif;
  background-color: #1d1227;
}
</style>