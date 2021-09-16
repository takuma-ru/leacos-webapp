<template>
  <div>
    {{ id }}
  </div>
</template>

<script lang="ts">
import { computed, defineComponent } from '@nuxtjs/composition-api'

export default defineComponent({
  setup (_, { root }) {
    const route = root.$route
    const id = computed(() => route.params.id)

    console.log(id)

    return {
      route,
      id
    }
  }
})
</script>
