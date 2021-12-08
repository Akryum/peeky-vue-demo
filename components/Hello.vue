<script setup lang="ts">
import { computed, ref } from 'vue'

const props = defineProps({
  count: {
    type: Number,
  }
})

const times = ref(2)

const result = computed(() => props.count * times.value)
</script>

<template>
  <pre>{{ count }} x {{ times }} = {{ result }}</pre>
  <button @click="times += 1">More</button>
</template>
