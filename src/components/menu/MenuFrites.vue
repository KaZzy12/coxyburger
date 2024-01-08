<template>
    <div v-for="(frite, idx) in frites" :key="idx">
        <h4>{{ frite.name }} | {{ $filters.currency(frite.price) }}</h4>
    </div>
</template>

<script>
/* eslint-disable import/no-named-as-default */
import menu from '../../menu/menu';

export default {
  name: 'MenuFrites',
  data() {
    return { frites: menu.frites };
  },
};
</script>
