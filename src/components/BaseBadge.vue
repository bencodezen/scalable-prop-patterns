<script>
export default {
  props: {
    type: {
      type: String,
      required: true
    },
    borderSide: {
      type: String,
      required: false
    },
    text: {
      type: String,
      required: true
    }
  }
}
</script>

<template>
  <div class="badge" :class="`is-${type} has-border-${borderSide}`">
    {{ text }}
  </div>
</template>

<style lang="scss" scoped>
.badge {
  padding: 0.5rem 0.75rem;
  background-color: #ccc;
  border-radius: 3px;
  color: #222;

  &.has-border-left {
    border-left: 8px solid #999;
  }

  &.has-border-right {
    border-right: 8px solid #999;
  }

  &.has-border-top {
    border-top: 8px solid #999;
  }

  &.has-border-bottom {
    border-bottom: 8px solid #999;
  }

  &.is-info {
    border-color: rgb(11, 73, 155);
    background-color: rgb(174, 204, 243);
  }

  &.is-success {
    border-color: rgb(35, 155, 11);
    background-color: rgb(174, 243, 174);
  }

  &.is-warning {
    border-color: rgb(155, 145, 11);
    background-color: rgb(242, 243, 174);
  }

  &.is-danger {
    border-color: rgb(155, 11, 11);
    background-color: rgb(245, 166, 166);
  }
}
</style>
