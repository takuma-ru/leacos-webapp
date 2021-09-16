<template>
  <div>
    {{ id }}
  </div>
</template>

<script lang="ts">
import { computed, defineComponent, useRoute } from '@nuxtjs/composition-api'

export default defineComponent({
  setup () {
    const route = useRoute()
    const id = computed(() => route.value.query.id) // ?id=asd

    return {
      route,
      id
    }
  }
})
</script>
