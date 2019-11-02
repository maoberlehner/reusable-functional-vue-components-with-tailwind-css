<template functional>
  <Component
    :is="props.tag"
    :ref="data.ref"
    class="px-6 py-4"
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
export const UiCardBody = {
  name: `UiCardBody`,
  props: {
    tag: {
      default: `div`,
      type: String,
    },
  },
};

export default UiCardBody;
</script>
