<template functional>
  <Component
    :is="props.tag"
    :ref="data.ref"
    class="container mx-auto px-4"
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
export const UiContainer = {
  name: `UiContainer`,
  props: {
    tag: {
      default: `div`,
      type: String,
    },
  },
};

export default UiContainer;
</script>
