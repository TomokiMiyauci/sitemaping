<template>
  <svg
    xmlns="http://www.w3.org/2000/svg"
    :width="width"
    :height="height"
    :viewBox="`0 0 24 24`"
    :aria-labelledby="iconName"
    role="presentation"
    class="inline"
  >
    <title lang="en">{{ iconName }}</title>
    <g :fill="iconColor">
      <slot />
    </g>
  </svg>
</template>

<script lang="ts">
  import { defineComponent } from 'vue'
  export default defineComponent({
    props: {
      iconName: {
        type: String,
        default: 'icon',
      },

      width: {
        type: [Number, String],
        default: 24,
      },

      height: {
        type: [Number, String],
        default: 24,
      },

      iconColor: {
        type: String,
        default: 'currentColor',
      },
    },
  })
</script>
