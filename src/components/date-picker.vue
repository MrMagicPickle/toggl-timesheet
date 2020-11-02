<template lang="pug">
.date-picker 
  button.left
    svg.bi.bi-arrow-bar-left(
      width="16px",
      height="16px",
      viewBox="0 0 16 16",
      fill="currentColor",
      xmlns="http://www.w3.org/2000/svg"
    )
      path(
        fill-rule="evenodd",
        d="M12.5 15a.5.5 0 0 1-.5-.5v-13a.5.5 0 0 1 1 0v13a.5.5 0 0 1-.5.5zM10 8a.5.5 0 0 1-.5.5H3.707l2.147 2.146a.5.5 0 0 1-.708.708l-3-3a.5.5 0 0 1 0-.708l3-3a.5.5 0 1 1 .708.708L3.707 7.5H9.5a.5.5 0 0 1 .5.5z"
      )
  .date-selector
    p This week
  button.right
    svg.bi.bi-arrow-bar-right(
      width="16px",
      height="16px",
      viewBox="0 0 16 16",
      fill="currentColor",
      xmlns="http://www.w3.org/2000/svg"
    )
      path(
        fill-rule="evenodd",
        d="M6 8a.5.5 0 0 0 .5.5h5.793l-2.147 2.146a.5.5 0 0 0 .708.708l3-3a.5.5 0 0 0 0-.708l-3-3a.5.5 0 0 0-.708.708L12.293 7.5H6.5A.5.5 0 0 0 6 8zm-2.5 7a.5.5 0 0 1-.5-.5v-13a.5.5 0 0 1 1 0v13a.5.5 0 0 1-.5.5z"
      )
</template>

<script>
export default {};
</script>

<style scoped lang="sass">
.date-picker
  background-color: white
  display: flex
  cursor: pointer

.left
  position: relative
  border: 1px solid #e3e3e3
  border-radius: 10px 0px 0px 10px
  width: 36px
  height: 36px
  background-color: white
  svg
    position: absolute
    left: 50%
    top: 50%
    transform: translate(-50%, -50%)

.date-selector
  width: 120px
  height: 36px
  background-color: white
  border-top: 1px solid #e3e3e3
  border-bottom: 1px solid #e3e3e3
  box-sizing: border-box
  display: flex
  justify-content: center
  align-items: center

  p
    font-size: 14px
    color: #000

.right
  border: 1px solid #e3e3e3
  border-radius: 0px 10px 10px 0px
  width: 36px
  height: 36px
  background-color: white
  position: relative
  svg
    position: absolute
    left: 50%
    top: 50%
    transform: translate(-50%, -50%)
</style>
