<script setup lang="ts">
import Header from '@/components/header/index.vue'
</script>

<template>
  <div class="flex h-screen w-full overflow-hidden bg-background text-foreground">
    <aside class="w-64 border-r border-border bg-card p-4">Sidebar Content</aside>

    <div class="flex flex-col flex-1">
      <header class="h-16 border-b border-border bg-background flex items-center px-6">
        <Header class="w-full" />
      </header>

      <main class="flex-1 overflow-y-auto bg-background p-6">
        <slot />
      </main>

      <footer
        class="h-12 border-t border-border bg-background flex items-center px-6 text-sm text-muted-foreground"
      >
        Footer / Status Bar
      </footer>
    </div>
  </div>
</template>
