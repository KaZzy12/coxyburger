<template>
    <div v-for="(sauce, idx) in sauces" :key="idx">
        <h4>{{ sauce.name }} | {{ $filters.currency(sauce.price) }}</h4>
    </div>
</template>

<script>
/* eslint-disable import/no-named-as-default */
import menu from '../../menu/menu';

export default {
  name: 'MenuFrites',
  data() {
    return { sauces: menu.sauces };
  },
};
</script>
