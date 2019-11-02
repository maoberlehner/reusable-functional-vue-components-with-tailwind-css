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
// TODO info in artikel, dass es hier verschiedene philosphien gibt und man das auch ohne abstraction, oder CSS class abstraktion machen könnte
// eventuell auch link zu CSS artikel wo steht wann abstraktion und so
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

