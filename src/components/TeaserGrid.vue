<template>
  <div class="md:flex -mx-3">
    <TeaserGridItem
      v-for="item in items"
      :key="item.id"
      :item="item"
      class="mx-3"
    />
  </div>
</template>

<script>
import TeaserGridItem from './TeaserGridItem.vue';

export default {
  name: `TeaserGrid`,
  components: {
    TeaserGridItem,
  },
  props: {
    items: {
      required: true,
      type: Array,
    },
  },
};
</script>
