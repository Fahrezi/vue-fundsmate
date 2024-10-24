<script setup lang="ts">
import { RouterLink } from "vue-router"
import { Menu } from "lucide-vue-next"
import { ref } from "vue"

const body = document.getElementsByTagName("body")[0]
const menu = ["What we offer", "Resource", "About us"]
const isMenuOpen = ref(false)

const handleMenu = () => {
  if (!isMenuOpen.value) {
    isMenuOpen.value = true
    body?.classList.add("overflow-hidden")
  } else {
    isMenuOpen.value = false
    body?.classList.remove("overflow-hidden")
  }
}
</script>

<template>
  <nav
    class="flex items-center justify-center gap-x-4 -mx-8 sm:mx-auto mb-8 relative"
  >
    <Menu class="block md:hidden float-end" @click="handleMenu" :size="20" />
    <span>
      <RouterLink class="font-bold text-2xl" to="/">fundsmate</RouterLink>
    </span>
    <ul class="items-center gap-x-8 mx-auto hidden md:flex">
      <li>
        <RouterLink class="font-semibold text-lg" to="/we-offer">
          What we offer
        </RouterLink>
      </li>
      <li>
        <RouterLink class="font-semibold text-lg" to="/resource">
          Resource
        </RouterLink>
      </li>
      <li>
        <RouterLink class="font-semibold text-lg" to="/about-us">
          About us
        </RouterLink>
      </li>
    </ul>
    <a
      class="py-2 px-6 text-primary border-2 border-primary rounded-full hidden sm:block"
      href="#"
    >
      Get Started
    </a>
    <div
      :class="`h-dvh bg-black/40 absolute top-[64px] w-full md:hidden ${isMenuOpen ? 'block' : 'hidden'}`"
    >
      <ul
        class="bg-[#faf8fd] flex flex-col gap-y-8 p-8 border-t border-gray-200"
      >
        <li v-for="item in menu" :key="item">
          <RouterLink class="font-semibold text-lg" to="/">{{
            item
          }}</RouterLink>
        </li>
        <a
          class="py-2 px-6 text-primary border-2 border-primary rounded-full block text-center sm:hidden"
          href="#"
        >
          Get Started
        </a>
      </ul>
    </div>
  </nav>
</template>
