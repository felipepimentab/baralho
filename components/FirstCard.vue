<template>
  <div
    class="first-card"
    :class="{'first-card--red': card.suit === 'copas' || card-suit === 'ouros'}"  
  >
    <div class="first-card__top">
      <span class="first-card__top__letter">{{ card.letter }}</span>
      <CardSuit
        class="first-card__top__suit"
        :suit="card.suit"
      />
    </div>
    <div class="first-card__middle">
      <p>{{ card.name }}</p>
    </div>
    <div class="first-card__bottom">
      <span class="first-card__top__letter">{{ card.letter }}</span>
      <CardSuit
        class="first-card__top__suit"
        :suit="card.suit"
      />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    card: {
      type: Object,
      required: true,
    }
  }
}
</script>

<style lang="scss" scoped>
.first-card {
  margin: 0 1rem 0.5rem 1rem;
  background-color: rgba($color: white, $alpha: 0.8);
  border-radius: 0.5rem;
  padding: 1rem;
  color: rgba($color: #000000, $alpha: 0.8);

  &__top, &__bottom {
    display: flex;
    align-items: center;

    &__letter {
      font-size: 3rem;
      font-family: 'Patua One', cursive;
    }

    &__suit {
      height: 2.3rem;
    }
  }

  &__middle {
    display: flex;
    justify-content: center;
    font-size: 2rem;
    margin: 0 2rem;
    border: 2px solid rgba($color: black, $alpha: 0.6);
    border-radius: 0.5rem;
  }

  &__bottom {
    transform: rotate(180deg);
  }

  &--red {
    color: rgba($color: rgb(160, 0, 0), $alpha: 0.8);

    .first-card__middle {
      border: 2px solid rgba($color: rgb(160, 0, 0), $alpha: 0.6);
    }
  }
}
</style>