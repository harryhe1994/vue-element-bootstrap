<template>
  <div class="header-view">
    <span class='title' align='left'>Vue Admin</span>
  </div>
</template>

<script>
export default {
  name: 'HeaderView',
};
</script>

<style lang="scss" scoped>
  .header-view {
    background-color: steelblue;
    width: 100%;
    height: 120px;
    .title {
      font-size: 22px;
      font-weight: 600;
      line-height: 58px;
      color: #ffffff;
      float: left;
      padding-left: 10px;
      cursor: pointer;
    }
  }
</style>
