<template>
  <div>
    <ul class="md:block max-w-6xl mx-auto">
      <li class="relative mb-8" v-for="(option, id) in searchOptions" :key="id">
        <Domains :Domains="option" :search-options="searchOptions" />
      </li>
    </ul>
  </div>
</template>
<script lang="ts" setup>
import { defineProps, toRefs } from "vue";
import { useQuery, useResult } from "@vue/apollo-composable";
import Domains from "./Domains.vue";

const props = defineProps({
  searchOptions: {
    type: Object,
    required: true
  }
});
</script>
