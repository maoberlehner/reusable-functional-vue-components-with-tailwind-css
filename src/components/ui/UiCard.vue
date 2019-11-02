<template functional>
  <Component
    :is="props.tag"
    :ref="data.ref"
    class="rounded overflow-hidden shadow-lg"
    :class="[
      data.class,
      data.staticClass,
    ]"
    :style="[
      data.style,
      data.staticStyle,
    ]"
    v-bind="data.attrs"
    v-on="listeners"
  >
    <slot/>
  </Component>
</template>

<script>
export { default as UiCardBody } from './UiCardBody.vue';

export const UiCard = {
  name: `UiCard`,
  props: {
    tag: {
      default: `div`,
      type: String,
    },
  },
};

export default UiCard;
</script>

