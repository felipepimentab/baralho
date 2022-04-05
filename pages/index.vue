<template>
  <div class="main">
    <FirstCard :card="store.getPlayedCards[0]" />
    <ul class="card-list">
      <li v-for="card in store.getPlayedCards.slice(1)" :key="card">
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
import { useCardStore } from "~/store/cards.js";
import CardSuit from '~/components/CardSuit.vue';
import FirstCard from '~/components/FirstCard.vue';

export default {
  name: 'IndexPage',

  components: {
    CardSuit,
    FirstCard,
  },

  setup() {
    const store = useCardStore();

    return { store };
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
      ],
    };
  },

  created() {
    this.store.resetDeck();
  },

  methods: {
    tirarCarta() {
      return null;
    }
  },
}
</script>

<style lang="scss" scoped>
.main {
  color: white;
  font-size: 1rem;
  height: calc(100vh - 9.25rem);
}

.card-list {
  width: 100%;
  padding: 0 1rem;
  margin: 0;
  list-style-type: none;
  max-height: calc(100vh - 24.25rem);
  overflow-y: auto;
  scroll-behavior: smooth;

  &__item {
    text-decoration: none;
    display: flex;
    align-items: center;
    padding: 0.5rem;
    margin: 0.5rem 0;
    /* From https://css.glass */
    background: rgba(255, 255, 255, 0.3);
    border-radius: 0.5rem;
    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
    /* backdrop-filter: blur(2.9px);
    -webkit-backdrop-filter: blur(2.9px); */

    &__icon {
      display: flex;
      align-items: center;
      padding: 0 1.5rem 0 0;

      &__letter {
        font-size: 2rem;
        margin: 0 0.3rem 0 0;
        width: 1.85rem;
        text-align: end;
        display: flex;
        flex-direction: row-reverse;
        font-family: 'Patua One', cursive;
      }

      &__suit {
        width: 1.5rem;
      }
    }

    &__name {
      margin: 0;
      font-size: 1.2rem;
      padding: 0;
      color: whitesmoke;
    }
  }

  &:first-child {
    font-size: 3rem;
  }
}
</style>