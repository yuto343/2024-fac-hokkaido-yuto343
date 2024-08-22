<template>
  <svg
    xmlns="http://www.w3.org/2000/svg"
    :width="size"
    :height="size"
    viewBox="0 0 1200 1200"
  >
    <path
      fill="white"
      d="m0 600l703.125 468.75V816.211H1200V383.789H703.125V131.25z"
    />
  </svg>
</template>

<script>
export default {
  props: {
    size: {
      type: Number,
      default: 128,
    },
  },
};
</script>
