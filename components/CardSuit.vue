<template>
  <component :is="`${suit}${alt ? 'Alt' : ''}`"></component>
</template>

<script>
import copas from '@/components/cards/Copas.vue';
import copasAlt from '@/components/cards/CopasAlt.vue';
import espadas from '@/components/cards/Espadas.vue';
import espadasAlt from '@/components/cards/EspadasAlt.vue';
import ouros from '@/components/cards/Ouros.vue';
import ourosAlt from '@/components/cards/OurosAlt.vue';
import paus from '@/components/cards/Paus.vue';
import pausAlt from '@/components/cards/PausAlt.vue';

export default {
  components: {
    copas,
    copasAlt,
    espadas,
    espadasAlt,
    ouros,
    ourosAlt,
    paus,
    pausAlt,
  },

  props: {
    suit: {
      type: String,
      required: true,
    },
    alt: {
      type: Boolean,
      required: false,
      default: false,
    }
  },

  methods: {
    suitIcon(suit) {
      switch(suit) {
        case 'copas':
          return 'Copas';
        case 'espadas':
          return 'Espadas';
        case 'ouros':
          return 'Ouros';
        case 'paus':
          return 'Paus';
        default:
          return null;         
      }
    }
  }
}
</script>