<template>
  <base-svg v-bind="$attrs">
    <path :d="mdiGoogle" />
  </base-svg>
</template>

<script lang="ts">
  import { mdiGoogle } from '@mdi/js'
  import { defineComponent } from 'vue'

  import BaseSvg from '/@/components/base/BaseSvg.vue'

  export default defineComponent({
    components: {
      BaseSvg,
    },

    setup() {
      return { mdiGoogle }
    },
  })
</script>
