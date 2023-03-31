<script setup lang="ts">
import { MainLayout } from '../components/layouts';
import { ButtonUI } from '../components/interface'
</script>

<template>
  <MainLayout>
    <main class="flex items-center justify-between -mt-8">
        <div class="md:w-1/2 text-[var(--color-text-3)]">
            <h1 class="text-lg md:text-xl !leading-6">Hello! I’m <span class="text-[var(--color-text-1)] font-bold">Meniks.</span></h1>
            <div class="my-4">
                <span class="text-[var(--color-text-2)] text-[3.375rem] leading-[125%]">{{'<Code Inspector/>'}}</span>
                <h2 class="text-[var(--color-text-1)] text-[4rem] leading-[80px] font-bold">Software Tester</h2>
            </div>
            <p class="w-4/5 text-sm text-justify !leading-[160%] tracking-[0.02em] mb-8">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nitsq nodol puren
            </p>
            <ButtonUI
                variant="primary"
                class="max-w-[13.25rem]"
            >
                Let’s talk
            </ButtonUI>
        </div>
        <div class="w-1/2 -mr-12">
            <img class="w-full" src="../assets/images/mk-landing-img.png" />
        </div>
    </main>
  </MainLayout>
</template>