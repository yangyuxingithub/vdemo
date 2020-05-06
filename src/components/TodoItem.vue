<template>
  <div>
    <!-- <span>{{auth}}</span> -->
    <p>子组件数值：{{cnum}}</p>
    <button @click="dianji(auth)">AddParentBtn</button>
  </div>
</template>

<script>
export default {
  props: {
    auth: {
      type: String,
      default: "children"
    },
    cnum: {
      type: Number,
      default: 666
    }
  },
  data() {
    return {};
  },
  components: {

  },
  methods: {
    dianji(e) {
      console.log(e);
      this.$emit("addParentNum", e);
    }
  }
};
</script>

<style scoped>
</style>
