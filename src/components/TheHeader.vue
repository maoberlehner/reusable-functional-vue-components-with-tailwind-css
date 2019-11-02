<template>
  <header class="border-b-2 border-gray-200 h-24 flex justify-between items-center">
    <a
      href="/"
      class="text-orange-500 text-3xl"
    >
      PUMPKIN
    </a>
    <nav class="flex text-xl">
      <a
        href="/"
        class="px-1 -ml-1 hover:undeline text-gray-700 hover:text-orange-500"
      >
        Home
      </a> |
      <a
        href="https://markus.oberlehner.net/blog/reusable-functional-vue-components-with-tailwind-css"
        class="px-1 hover:undeline text-gray-700 hover:text-orange-500"
      >
        About
      </a>
    </nav>
  </header>
</template>

<script>
export default {
  name: `TheHeader`,
};
</script>
