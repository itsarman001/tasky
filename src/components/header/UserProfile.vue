<script setup lang="ts">
import { Avatar, AvatarFallback, AvatarImage } from '@/components/ui/avatar'
// import { Separator } from '@/components/ui/separator'
</script>

<template>
  <!-- TODO: Separator  -->
  <div class="flex items-center gap-4 border-l-2 border-border pl-2 ml-2">
    <div>Name</div>
    <Avatar>
      <AvatarImage src="https://github.com/shadcn.png" alt="@shadcn" />
      <AvatarFallback>CN</AvatarFallback>
    </Avatar>
  </div>
</template>
