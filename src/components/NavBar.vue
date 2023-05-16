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
    <nav class="nav">
      <div class="spacer" />
      <div class="right">
        <router-link to="posts" title="Blog">
          <span class="lt-md:hidden">Blog</span>
          <div i-ri-article-line md:hidden />
        </router-link>
        <router-link to="/projects" title="Projects">
          <span class="lt-md:hidden">Projects</span>
          <div i-ri-lightbulb-line md:hidden />
        </router-link>
        <a href="https://github.com/hglong16" target="_blank" title="Github">
          <div i-uil-github-alt />
        </a>
        <toggle-theme />
      </div>
    </nav>
  </header>
</template>
