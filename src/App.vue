<template>
  <div class="bg-background font-body text-on-surface min-h-screen flex flex-col">
    <main class="flex-1 flex flex-col md:flex-row items-center justify-center p-6 gap-12">
      <HeroDisplay />
      <div class="hidden md:block self-stretch border-l-2 border-dashed border-outline-variant/70"></div>
      <LoginForm />
    </main>
    <SiteFooter />
  </div>
</template>

<script setup>
import HeroDisplay from './component/HeroDisplay.vue'
import LoginForm from './component/LoginForm.vue'
import SiteFooter from './component/SiteFooter.vue'
</script>

<style>
</style>