<template>
  <div class="mdl-layout__header-row">
    <span class="mdl-layout-title" v-if="title">{{title}}</span>
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: {
    title: [Boolean, String]
  },
  mounted () {
    componentHandler.upgradeElement(this.$el)
  }
}
</script>
