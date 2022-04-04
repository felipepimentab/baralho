<template>
  <div class="main">
    <ul class="card-list">
      <li v-for="card in deck" :key="card">
        <div class="card-list__item">
          <div class="card-list__item__icon">
            <p class="card-list__item__icon__letter">
              {{ card.letter }}
            </p>
            <CardSuit
              class="card-list__item__icon__suit"
              :suit="card.suit"
            />
          </div>
          <p class="card-list__item__name">{{ card.name }}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
import CardSuit from '~/components/CardSuit.vue';

export default {
  name: 'IndexPage',

  components: {
    CardSuit,
  },

  data() {
    return {
      deck: [
        {
          name: "Ás de Espadas",
          suit: "espadas",
          letter: "A",
        },
        {
          name: "Ás de Paus",
          suit: "paus",
          letter: "A",
        },
        {
          name: "Ás de Copas",
          suit: "copas",
          letter: "A",
        },
        {
          name: "Ás de Ouros",
          suit: "ouros",
          letter: "A",
        },
        {
          name: "Dois de Espadas",
          suit: "espadas",
          letter: "2",
        },
        {
          name: "Dois de Paus",
          suit: "paus",
          letter: "2",
        },
        {
          name: "Dois de Copas",
          suit: "copas",
          letter: "2",
        },
        {
          name: "Dois de Ouros",
          suit: "ouros",
          letter: "2",
        },
        {
          name: "Três de Espadas",
          suit: "espadas",
          letter: "3",
        },
        {
          name: "Três de Paus",
          suit: "paus",
          letter: "3",
        },
        {
          name: "Três de Copas",
          suit: "copas",
          letter: "3",
        },
        {
          name: "Três de Ouros",
          suit: "ouros",
          letter: "3",
        },
        {
          name: "Quatro de Espadas",
          suit: "espadas",
          letter: "4",
        },
        {
          name: "Quatro de Paus",
          suit: "paus",
          letter: "4",
        },
        {
          name: "Quatro de Copas",
          suit: "copas",
          letter: "4",
        },
        {
          name: "Quatro de Ouros",
          suit: "ouros",
          letter: "4",
        },
        {
          name: "Cinco de Espadas",
          suit: "espadas",
          letter: "5",
        },
        {
          name: "Cinco de Paus",
          suit: "paus",
          letter: "5",
        },
        {
          name: "Cinco de Copas",
          suit: "copas",
          letter: "5",
        },
        {
          name: "Cinco de Ouros",
          suit: "ouros",
          letter: "5",
        },
        {
          name: "Seis de Espadas",
          suit: "espadas",
          letter: "6",
        },
        {
          name: "Seis de Paus",
          suit: "paus",
          letter: "6",
        },
        {
          name: "Seis de Copas",
          suit: "copas",
          letter: "6",
        },
        {
          name: "Seis de Ouros",
          suit: "ouros",
          letter: "6",
        },
        {
          name: "Sete de Espadas",
          suit: "espadas",
          letter: "7",
        },
        {
          name: "Sete de Paus",
          suit: "paus",
          letter: "7",
        },
        {
          name: "Sete de Copas",
          suit: "copas",
          letter: "7",
        },
        {
          name: "Sete de Ouros",
          suit: "ouros",
          letter: "7",
        },
        {
          name: "Oito de Espadas",
          suit: "espadas",
          letter: "8",
        },
        {
          name: "Oito de Paus",
          suit: "paus",
          letter: "8",
        },
        {
          name: "Oito de Copas",
          suit: "copas",
          letter: "8",
        },
        {
          name: "Oito de Ouros",
          suit: "ouros",
          letter: "8",
        },
        {
          name: "Nove de Espadas",
          suit: "espadas",
          letter: "9",
        },
        {
          name: "Nove de Paus",
          suit: "paus",
          letter: "9",
        },
        {
          name: "Nove de Copas",
          suit: "copas",
          letter: "9",
        },
        {
          name: "Nove de Ouros",
          suit: "ouros",
          letter: "9",
        },
        {
          name: "Dez de Espadas",
          suit: "espadas",
          letter: "10",
        },
        {
          name: "Dez de Paus",
          suit: "paus",
          letter: "10",
        },
        {
          name: "Dez de Copas",
          suit: "copas",
          letter: "10",
        },
        {
          name: "Dez de Ouros",
          suit: "ouros",
          letter: "10",
        },
        {
          name: "Valete de Espadas",
          suit: "espadas",
          letter: "J",
        },
        {
          name: "Valete de Paus",
          suit: "paus",
          letter: "J",
        },
        {
          name: "Valete de Copas",
          suit: "copas",
          letter: "J",
        },
        {
          name: "Valete de Ouros",
          suit: "ouros",
          letter: "J",
        },
        {
          name: "Dama de Espadas",
          suit: "espadas",
          letter: "Q",
        },
        {
          name: "Dama de Paus",
          suit: "paus",
          letter: "Q",
        },
        {
          name: "Dama de Copas",
          suit: "copas",
          letter: "Q",
        },
        {
          name: "Dama de Ouros",
          suit: "ouros",
          letter: "Q",
        },
        {
          name: "Rei de Espadas",
          suit: "espadas",
          letter: "K",
        },
        {
          name: "Rei de Paus",
          suit: "paus",
          letter: "K",
        },
        {
          name: "Rei de Copas",
          suit: "copas",
          letter: "K",
        },
        {
          name: "Rei de Ouros",
          suit: "ouros",
          letter: "K",
        },
      ],
      cartasEmJogo: [],
      cartasJogadas: [],
    }
  },

  methods: {
    tirarCarta() {
      return null;
    }
  }
}
</script>

<style lang="scss" scoped>
.main {
  color: white;
  font-size: 1rem;
}

.card-list {
  width: calc(100% - 2rem);
  padding: 0 1rem;
  margin: 0;
  list-style-type: none;
  max-height: calc(100vh - 10rem);
  overflow-y: auto;
  scroll-behavior: smooth;

  &__item {
    text-decoration: none;
    display: flex;
    align-items: center;
    padding: 0.5rem;
    margin: 0.5rem 0;
    /* From https://css.glass */
    background: rgba(255, 255, 255, 0.5);
    border-radius: 16px;
    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
    /* backdrop-filter: blur(2.9px);
    -webkit-backdrop-filter: blur(2.9px); */

    &__icon {
      display: flex;
      align-items: center;
      padding: 0 1.5rem 0 0.5rem;

      &__letter {
        font-size: 2rem;
        margin: 0 0.3rem 0 0;
        font-family: 'Patua One', cursive;
      }

      &__suit {
        width: 2rem;
      }
    }

    &__name {
      margin: 0;
      font-size: 1.2rem;
      padding: 0;
      color: black;
    }
  }

  &:first-child {
    font-size: 3rem;
  }
}
</style>