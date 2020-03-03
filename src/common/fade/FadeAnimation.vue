<template>
    <transition>
      <slot></slot>
    </transition>
</template>

<script>
export default {
  name: 'FadeAnimation'
}
</script>

<style lang="stylus" scoped>
  .v-enter, .vleave-to
    opacity: 0
  .v-enter-active, .v-leave-active
    transition: opacity .5s
</style>
