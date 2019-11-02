<template>
  <AppHero>
    <UiHeadline :level="1">
      Lorem Ipsum dolor
      <span class="sm:block text-orange-500 font-normal">
        eirmod tempor invidunt ut.
      </span>
    </UiHeadline>
    <p class="mt-6 leading-relaxed sm:text-lg md:text-xl xl:text-lg text-gray-700">
      Tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos
      et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata
      sanctus est Lorem ipsum dolor sit amet.
    </p>
    <img
      slot="figure"
      src="https://images.unsplash.com/photo-1572510176982-e9b0dac331d2?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=600&q=80"
      alt="Halloween pumpkin."
    >
  </AppHero>
</template>

<script>
import { UiHeadline } from './ui/UiHeadline.vue';
import AppHero from './AppHero.vue';

export default {
  name: `TheHero`,
  components: {
    AppHero,
    UiHeadline,
  },
};
</script>
