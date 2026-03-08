<script setup lang="ts">
import UserProfile from '@/components/header/UserProfile.vue'
import ThemeToggle from '@/components/common/ThemeToggle.vue'
import Notification from '@/components/common/Notification.vue'
</script>
<template>
  <div class="flex items-center w-full">
    <div>Breadcrumbs</div>
    <div class="flex items-center gap-2 ml-auto">
      <Notification />
      <ThemeToggle />
      <UserProfile />
    </div>
  </div>
</template>
