<script setup lang="ts"></script>

<template>
  <div class="flex h-screen w-full overflow-hidden bg-slate-900 text-white">
    <aside class="w-64 border-r border-slate-700 bg-slate-800 p-4">Sidebar Content</aside>

    <div class="flex flex-col flex-1">
      <header class="h-16 border-b border-slate-700 bg-slate-800 flex items-center px-6">
        Header / Breadcrumbs
      </header>

      <main class="flex-1 overflow-y-auto bg-slate-900 p-6">
        <slot />
      </main>

      <footer
        class="h-12 border-t border-slate-700 bg-slate-800 flex items-center px-6 text-sm text-slate-400"
      >
        Footer / Status Bar
      </footer>
    </div>
  </div>
</template>
