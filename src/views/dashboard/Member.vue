<template lang="pug">
.member
  .main
    SideNav
    .content-container
      HeaderBar
      FilterBar
      .content
        .datepicker-container
          DatePicker
</template>

<script>
export default {
  components: {
    SideNav: () => import("../../components/side-nav.vue"),
    HeaderBar: () => import("../../components/header-bar.vue"),
    FilterBar: () => import("../../components/filter-bar.vue"),
    DatePicker: () => import("../../components/date-picker.vue"),
  },
  data() {
    return {
      name: "Wei Shen",
    };
  },
};
</script>

<style scoped lang="sass">
.member
  width: 100%
  height: 100%

.main
  display: flex
  width: 100%
  height: 100%

.content-container
  flex-grow: 1
  height: 100%

.content
  width: 100%
  height: 100%
  position: relative
  background-color: #fef9f8

.datepicker-container
  position: absolute
  top: 20px
  left: 20px
</style>
