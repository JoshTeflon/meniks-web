<script setup lang="ts">
import { MainLayout } from '../layouts';
import { ButtonUI } from '../interface';
//     defineProps<{
//   msg: string
// }>()
const navItems = ['home', 'experience', 'contact']
</script>

<template>
  <MainLayout>
    <nav class="w-full md:h-24 flex border border-[var(--mk-text-light-2)] my-11">
      <div class="w-1/5 flex items-center justify-center border-r border-[var(--mk-text-light-2)]">
        <img src="../../assets/images/EMI.png" class="w-28 md:32" />
      </div>
      <div
        v-for="(items, index) in navItems"
        :key="index"
        class="w-1/5 border-r border-[var(--mk-text-light-2)] text-[var(--color-text-1)] text-sm flex items-center justify-center uppercase tracking-[0.06em]"
      >
        {{  items  }}
      </div>
      <div class="w-1/5 flex items-center justify-center">
        <ButtonUI
          class="max-w-[7rem] mx-auto"
          variant="primary-outline"
        >
          Resume
        </ButtonUI>
      </div>
    </nav>
  </MainLayout>
</template>