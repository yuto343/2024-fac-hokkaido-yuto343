<template>
  <div class="slidev-layout container">
    <div class="my-auto text-center inline-block relative">
      <div class="text-5 subtitle"><slot name="subtitle" /></div>
      <slot />
    </div>
  </div>
</template>
<style scoped>
.container {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}
.subtitle {
  text-align: left;
}
</style>
