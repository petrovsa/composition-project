<script setup>
import { ClockIcon, ListBulletIcon, ChartBarIcon } from "@heroicons/vue/24/outline";
import NavItem from "./NavItem.vue";

const navItems = {
  timeline: ClockIcon,
  activities: ListBulletIcon,
  progress: ChartBarIcon
  
};
</script>

<template>
  <nav class="sticky bottom-0 z-20 bg-white">
    <ul class="flex justify-around items-center border-t">
      <NavItem 
        :href="`#${page}`" 
        v-for="icon, page, idx in navItems" 
        :key="idx"
      >
        <component :is="icon" class="h-6 w-6"/>
            {{ page }}
      </NavItem>
    </ul>
  </nav>
</template>