<script setup lang="ts">
import { FolderCode } from 'lucide-vue-next'
import {
  Empty,
  EmptyContent,
  EmptyDescription,
  EmptyHeader,
  EmptyMedia,
  EmptyTitle,
} from '@/components/ui/empty'

defineProps({
  title: {
    type: String,
    default: 'Title of the empty state.',
  },
  description: {
    type: String,
    default: 'Description of the empty state.',
  },
})
</script>

<template>
  <Empty>
    <EmptyHeader>
      <EmptyMedia variant="icon">
        <slot name="icon">
          <FolderCode />
        </slot>
      </EmptyMedia>
      <EmptyTitle>{{ title }}</EmptyTitle>
      <EmptyDescription>
        {{ description }}
      </EmptyDescription>
    </EmptyHeader>
    <EmptyContent>
      <slot />
    </EmptyContent>
    <slot name="append" />
  </Empty>
</template>
