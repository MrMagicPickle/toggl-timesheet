<template lang="pug">
.header-bar
  .submission
    p Submission
  .invite-members
    p Invite Members
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
.header-bar
  width: 100%
  height: 66px
  display: flex
  border-bottom: 1px solid #e3e3e3
  align-items: center
.submission
  font-size: 16px
  flex-grow: 1
  padding-left: 10px
  text-align: left
  font-weight: bold
  p
    color: #2c1338

.invite-members
  padding-right: 10px
</style>
