<script setup lang="ts">
import { isDark } from "~/logics";
</script>
<template>
  <header class="header-z40">
    <RouterLink
      class="w-10 h-10 absolute lg:fixed m-6 select-none-outline-none"
      to="/"
      focusable="false"
    >
      <img v-show="isDark" src="/logo-dark.svg?url" alt="logo" />
      <img v-show="!isDark" src="/logo.svg?url" alt="logo" />
    </RouterLink>
  </header>
</template>
