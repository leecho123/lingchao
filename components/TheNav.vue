<script setup lang="ts">
import { nav } from '~/constants'

const isOpen = ref(false)
</script>

<template>
  <nav
    class="
      sticky top-0 z-50 p-4 backdrop-blur bg-primary-400/10
      backdrop-saturate-50 flex items-center justify-between
    "
  >
    <span class="flex items-center font-bold">
      <Logos class="w-8 h-8 mr-2 " />
      Spiritual <span class="text-primary">Tide</span>
    </span>
    <!-- 桌面和平板 -->
    <ul class="hidden sm:flex gap-x-4">
      <li v-for="item of nav" :key="item.to" class="relative">
        <NuxtLink class="hover:text-primary before:transition-all before:contents-[''] before:absolute before:h-0.5 before:w-0 before:bg-primary-700 before:-bottom-1 hover:before:w-full" active-class="text-primary" :to="item.to">
          {{ item.title }}
        </NuxtLink>
      </li>
    </ul>
    <!-- 移动端 -->
    <span class="flex items-center space-x-2">
      <DarkToggle />
      <UButton
        class="sm:hidden"
        variant="link"
        square
        icon="i-carbon-list"
        color="white"
        @click="isOpen = true"
      />
    </span>
    <USlideover
      v-model="isOpen"
      :ui="{
        width: 'max-w-xs',
      }"
    >
      <div class="p-4">
        <h1 class="text-xl font-bold">
          lingchao.com
        </h1>
      </div>
    </USlideover>
  </nav>
</template>
