<template functional>
  <Component
    :is="props.tag"
    :ref="data.ref"
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
export const UiCardFigure = {
  name: `UiCardFigure`,
  props: {
    tag: {
      default: `div`,
      type: String,
    },
  },
};

export default UiCardFigure;
</script>
