<script setup lang="ts">
import { FolderKanban, ArrowUpRightIcon } from 'lucide-vue-next'
import { Button } from '@/components/ui/button'
import EmptyPage from '@/components/common/EmptyPage.vue'
import { RouterLink } from 'vue-router'
</script>

<template>
  <EmptyPage
    title="Boards Coming Soon"
    description="Boards will help you organize tasks and manage workflows visually."
  >
    <template #icon>
      <FolderKanban />
    </template>

    <template #actions>
      <Button disabled>Coming Soon</Button>
    </template>

    <template #append>
      <Button variant="link" size="sm" class="text-muted-foreground" as-child>
        <RouterLink to="/"> Go to Home <ArrowUpRightIcon class="ml-1 size-4" /> </RouterLink>
      </Button>
    </template>
  </EmptyPage>
</template>
