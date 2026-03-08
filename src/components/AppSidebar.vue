<script setup lang="ts">
import { Calendar, LayoutDashboard, FolderKanban, Users, GalleryVerticalEnd } from 'lucide-vue-next'
import {
  Sidebar,
  SidebarHeader,
  SidebarContent,
  SidebarGroup,
  SidebarGroupContent,
  SidebarGroupLabel,
  SidebarMenu,
  SidebarMenuButton,
  SidebarMenuItem,
} from '@/components/ui/sidebar'
import { RouterLink } from 'vue-router'

// Menu items.
const items = [
  {
    label: 'Dashboard',
    path: '/dashboard',
    icon: LayoutDashboard,
  },
  {
    label: 'Boards',
    path: '/boards',
    icon: FolderKanban,
  },
  {
    label: 'Calendar',
    path: '/calendar',
    icon: Calendar,
  },
  {
    label: 'Team',
    path: '/team',
    icon: Users,
  },
]
</script>

<template>
  <Sidebar variant="floating" collapsible="icon">
    <!-- Sidebar Header -->
    <SidebarHeader>
      <SidebarMenu>
        <SidebarMenuItem>
          <SidebarMenuButton size="lg">
            <div
              class="flex aspect-square size-8 items-center justify-center rounded-lg bg-sidebar-primary text-sidebar-primary-foreground"
            >
              <GalleryVerticalEnd class="size-4" />
            </div>
            <div class="grid flex-1 text-left text-sm leading-tight">
              <span class="truncate font-semibold">Tasky</span>
              <span class="truncate text-xs">Personal Task Manager</span>
            </div>
          </SidebarMenuButton>
        </SidebarMenuItem>
      </SidebarMenu>
    </SidebarHeader>

    <!-- Sidebar Content -->
    <SidebarContent>
      <SidebarGroup>
        <SidebarGroupLabel>Panels</SidebarGroupLabel>
        <SidebarGroupContent>
          <SidebarMenu>
            <SidebarMenuItem v-for="item in items" :key="item.label">
              <SidebarMenuButton as-child>
                <RouterLink :to="item.path">
                  <component :is="item.icon" />
                  <span>{{ item.label }}</span>
                </RouterLink>
              </SidebarMenuButton>
            </SidebarMenuItem>
          </SidebarMenu>
        </SidebarGroupContent>
      </SidebarGroup>
    </SidebarContent>
  </Sidebar>
</template>
