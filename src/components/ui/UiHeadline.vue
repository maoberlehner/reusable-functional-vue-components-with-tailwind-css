<template functional>
  <Component
    :is="props.tag || `h${props.level}`"
    :ref="data.ref"
    class="font-light leading-tight"
    :class="[
      ...((props.size || props.level) === 1 ? [`text-3xl sm:text-4xl md:text-5xl`] : []),
      ...((props.size || props.level) === 2 ? [`text-2xl sm:text-3xl md:text-4xl`] : []),
      ...((props.size || props.level) === 3 ? [`text-1xl sm:text-2xl md:text-3xl`] : []),
      ...((props.size || props.level) >= 4 ? [`text-xl sm:text-1xl md:text-2xl`] : []),
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
export const UiHeadline = {
  name: `UiHeadline`,
  props: {
    level: {
      required: true,
      type: Number,
      validator(value) {
        // Here PurgeCSS picks up the selectors and
        // does not remove their styles from the CSS.
        const headlines = [`h1`, `h2`, `h3`, `h4`, `h5`, `h6`];
        return headlines.includes(`h${value}`);
      },
    },
    size: {
      default: null,
      type: Number,
    },
    tag: {
      default: null,
      type: String,
    },
  },
};

export default UiHeadline;
</script>
