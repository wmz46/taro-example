<script setup lang="ts">
import { useSlots } from 'vue';
const slots = useSlots();
</script>
<template>
  <nut-button v-bind="$attrs">
    <template v-for="(_, name) in slots" #[name]="slotProps">
      <slot :name="name" v-bind="slotProps || {}" />
    </template>
  </nut-button>
</template>