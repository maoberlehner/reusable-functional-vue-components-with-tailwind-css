<template>
  <UiContainer>
    <TheHeader/>
    <TheHero/>
    <main class="py-12">
      <TeaserGrid :items="teaserItems"/>
    </main>
    <TheFooter/>
  </UiContainer>
</template>

<script>
import { UiContainer } from './components/ui/UiContainer.vue';
import TeaserGrid from './components/TeaserGrid.vue';
import TheFooter from './components/TheFooter.vue';
import TheHeader from './components/TheHeader.vue';
import TheHero from './components/TheHero.vue';

const teaserItems = [
  {
    id: 1,
    image: {
      alt: `Halloween pumpkin.`,
      src: `https://images.unsplash.com/photo-1572510192261-e24ab8f31042?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=600&h=400&q=80`,
    },
    text: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium.`,
    title: `Dolor sit amet`,
  },
  {
    id: 2,
    image: {
      alt: `Halloween pumpkin.`,
      src: `https://images.unsplash.com/photo-1534337711732-1c9ae62389e2?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&h=400&q=80`,
    },
    text: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium.`,
    title: `Consectetur adipisicing`,
  },
  {
    id: 3,
    image: {
      alt: `Halloween pumpkin.`,
      src: `https://images.unsplash.com/photo-1572510176982-e9b0dac331d2?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=600&h=400&q=80`,
    },
    text: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium.`,
    title: `Voluptatibus quia`,
  },
];

export default {
  name: `App`,
  components: {
    TeaserGrid,
    TheFooter,
    TheHeader,
    TheHero,
    UiContainer,
  },
  created() {
    this.teaserItems = teaserItems;
  },
};
</script>
