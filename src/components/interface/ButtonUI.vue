<script setup lang="ts">
export interface ButtonProps {
  variant?: 'primary' | 'primary-outline'
  type?: 'button' | 'submit'
}

const props = withDefaults(defineProps<ButtonProps>(), {
  variant: 'primary',
  type: 'button'
})
</script>

<template>
  <button :class="[$style.base, $style[variant]]">
    <slot />
  </button>
</template>

<style module scoped>
.base {
  @apply w-full text-sm md:text-base font-medium text-inherit !leading-4 flex items-center justify-center p-4 outline-none;
}

.primary {
  @apply bg-[var(--mk-cta)] text-[var(--mk-white)] rounded-[32px] p-[1.15rem];
}

.primary-outline {
  @apply bg-transparent text-[var(--mk-cta)] border-2 border-[var(--mk-cta)] rounded-[32px];
}
</style>