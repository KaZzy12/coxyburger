<template>
    <div v-for="(snack, idx) in snacks" :key="idx">
        <h4>{{ snack.name }} | {{ $filters.currency(snack.price) }}</h4>
    </div>
</template>

<script>
/* eslint-disable import/no-named-as-default */
import menu from '../../menu/menu';

export default {
  name: 'MenuFrites',
  data() {
    return { snacks: menu.snacks };
  },
};
</script>
