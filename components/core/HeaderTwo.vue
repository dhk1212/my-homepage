<template>
  <h2 class="text-colar_pink font-bold text-xl tracking-wider">
    {{ text }}
  </h2>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      required: true,
    },
  },
}
</script>
