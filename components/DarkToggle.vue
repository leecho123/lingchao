<script setup lang="ts">
const colorMode = useColorMode()
const isDark = ref(colorMode.value === 'dark')
function toggle() {
  colorMode.preference = colorMode.value === 'dark' ? 'light' : 'dark'
}
</script>

<template>
  <UToggle
    v-model="isDark"
    on-icon="i-carbon-moon"
    off-icon="i-carbon-sun"
    @change="toggle"
  />
</template>
