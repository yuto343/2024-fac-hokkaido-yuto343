<template>
  <div class="slidev-layout">
    <slot />
    <div class="outer">
      <div class="left"><slot name="left" /></div>
      <div class="right">
        <slot name="right" />
      </div>
    </div>
  </div>
</template>

<style scoped>
.outer {
  display: flex;
  justify-content: space-between;
}
.left {
  width: 45%;
}
.right {
  width: 45%;
}
</style>
