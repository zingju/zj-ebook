<template>
  <div class="home">
    <span class="icon-add"></span>
    <span class="test">ABCD</span>
  </div>
</template>
<script>
import { mapGetters } from "vuex";
export default {
  computed: {
    ...mapGetters(["test"]),
  },
  mounted() {
    this.$store.dispatch("setTest", 11).then(() => {
      console.log(this.test);
    });
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/css/global.scss";
.icon-add {
  font-size: px2rem(30);
  color: red;
}
.test {
  font-family: "Days One";
  font-size: px2rem(30);
}
</style>
