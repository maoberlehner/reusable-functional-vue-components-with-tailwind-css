<template>
  <UiCard>
    <UiCardFigure
      tag="img"
      :alt="item.image.alt"
      :src="item.image.src"
    />
    <UiCardBody class="text-gray-700">
      <UiHeadline
        :level="2"
        :size="4"
        class="font-bold"
      >
        {{ item.title }}
      </UiHeadline>
      <p class="mt-2">
        {{ item.text }}
      </p>
    </UiCardBody>
  </UiCard>
</template>

<script>
import { UiCard, UiCardBody, UiCardFigure } from './ui/UiCard.vue';
import { UiHeadline } from './ui/UiHeadline.vue';

export default {
  name: `TeaserGridItem`,
  components: {
    UiCard,
    UiCardBody,
    UiCardFigure,
    UiHeadline,
  },
  props: {
    item: {
      required: true,
      type: Object,
    },
  },
};
</script>
