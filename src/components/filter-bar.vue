<template lang="pug">
.filter-bar
  .filter-by
    p Filter By:
  .item
    p Team
  .item
    p Client
  .item
    p Project
</template>

<script>
export default {
  data() {
    return {
      name: "Wei Shen",
    };
  },
};
</script>

<style scoped lang="sass">
.filter-bar
  display: flex
  width: 100%
  height: 50px
  font-size: 14px
  position: relative
  box-shadow: rgb(232, 232, 232) 0px 8px 4px -4px
  z-index: 100

.filter-by
  padding: 0px 20px

.item
  padding: 0px 10px
</style>
