<template>
  <div class="w-full border-b flex items-center justify-center bg-black">
    <div
      class="flex items-center justify-between px-4 text-black d md:px-8 py-2"
    >
      <div class="flex items-center">
        <nuxt-link
          to="/"
          class="md:flex text-sm sm:text-lg md:text-2xl font-mono text-gray-200"
        >
          AXK
        </nuxt-link>
      </div>
      <button @click="toggleMenu()" class="md:hidden p-2 rounded">
        <Icon
          :name="isMenuOpen ? 'pajamas:close' : 'pajamas:hamburger'"
          class="w-6 h-6 text-gray-300"
        />
      </button>
      <!-- Desktop menu -->
      <ul
        class="hidden md:flex text-sm sm:text-lg md:text-2xl flex-row text-gray-200 text-shadow navbar font-mono"
      >
        <li class="hover:scale-110">
          <p class="pl-4 sm:pl-8 md:pl-12 lg:pl-16">Home</p>
        </li>
        <li class="hover:scale-110">
          <p class="pl-4 sm:pl-8 md:pl-12 lg:pl-16">About</p>
        </li>
        <li class="hover:scale-110">
          <p class="pl-4 sm:pl-8 md:pl-12 lg:pl-16">Services</p>
        </li>

        <li class="hover:scale-110">
          <p class="pl-4 sm:pl-8 md:pl-12 lg:pl-16">Contact</p>
        </li>
      </ul>
    </div>
    <ul
      v-if="isMenuOpen"
      class="block md:hidden mt-56 absolute z-10 m-auto left-0 w-2/4 right-0 border rounded-lg text-center font-mono bg-black"
    >
      <li>
        <nuxt-link
          to="/"
          class="block py-2 px-4 text-gray-200 pl-8 hover:scale-110"
          aria-current="page"
          >Home</nuxt-link
        >
      </li>
      <li>
        <p class="block py-2 px-4 text-gray-200 pl-8 hover:scale-110">
          Portfolio
        </p>
      </li>
      <li>
        <p
          class="block py-2 px-4 text-gray-200 pl-8 hover:scale-110"
          aria-current="page"
        >
          About
        </p>
      </li>
      <li>
        <p class="block py-2 px-4 text-gray-200 pl-8 hover:scale-110">
          Contact
        </p>
      </li>
    </ul>
  </div>
</template>
<script setup>
const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};
// Add event listener to close the menu when clicking outside
</script>
