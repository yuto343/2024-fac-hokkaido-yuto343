<template>
  <div class="slidev-layout section w-full h-full grid">
    <div class="my-auto text-center inline-block relative">
      <span class="text-5"><slot name="subtitle" /></span>
      <slot />
    </div>
  </div>
</template>
<style scoped>
span {
  position: absolute;
  top: -120%;
  left: 20%;
}
</style>
