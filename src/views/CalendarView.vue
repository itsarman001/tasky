<script setup lang="ts">
import { Calendar, ArrowUpRightIcon } from 'lucide-vue-next'
import { Button } from '@/components/ui/button'
import EmptyPage from '@/components/common/EmptyPage.vue'
import { RouterLink } from 'vue-router'
</script>

<template>
  <EmptyPage
    title="Calendar Coming Soon"
    description="The calendar will allow you to schedule tasks, events, and deadlines."
  >
    <template #icon>
      <Calendar />
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
