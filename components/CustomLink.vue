<template>
  <NuxtLink v-bind="props">
    <slot />
  </NuxtLink>
</template>

<script lang="ts" setup>
import type { NuxtLinkProps } from '#app'

interface CustomLinkProps extends Omit<NuxtLinkProps, 'to'> {
  to: string
}

const props = defineProps<CustomLinkProps>()
</script>
