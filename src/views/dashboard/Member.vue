<template lang="pug">
.member
  .main
    SideNav
    .content-container
      HeaderBar
      FilterBar
      .content(
        @drop.stop.prevent="handleDrop",
        @dragover.stop.prevent="handleDragOver",
        @dragleave.stop.prevent="handleDragLeave"
      )
        .days-container
          .day(v-for="(day, index) in days", :key="'day-' + index")
            p {{ day }}
            input(type="text")

        .datepicker-container
          DatePicker
</template>

<script>
import Papa from "papaparse";
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
      userData: [],
      days: [
        "Monday",
        "Tuesday",
        "Wednesday",
        "Thursday",
        "Friday",
        "Saturday",
        "Sunday",
      ],
    };
  },
  methods: {
    handleDrop(e) {
      const reader = new FileReader();
      reader.onloadend = () => {
        const { data, errors } = Papa.parse(reader.result, { header: true });
        const errRows = errors.map((x) => x.row);
        const actualData = [];
        for (let i = 0; i < data.length; i++) {
          if (!errRows.includes(i)) {
            actualData.push(data[i]);
          }
        }
        this.userData = actualData;
      };
      reader.readAsBinaryString(e.dataTransfer.files[0]);
    },
    handleDragOver(e) {
      console.log("Drag Over ---");
      console.log(e);
    },
    handleDragLeave(e) {
      console.log("Drag leave ---");
      console.log(e);
    },
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

.days-container
  display: flex
</style>
