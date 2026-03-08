<script setup lang="ts">
import { Users, ArrowUpRightIcon } from 'lucide-vue-next'
import { Button } from '@/components/ui/button'
import EmptyPage from '@/components/common/EmptyPage.vue'
import { RouterLink } from 'vue-router'
</script>

<template>
  <EmptyPage
    title="Team Management Coming Soon"
    description="Invite teammates, assign roles, and collaborate with your team."
  >
    <template #icon>
      <Users />
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
