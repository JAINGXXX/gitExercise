<template>
  <div id="app">
    <component :is="elect"></component>
    <TabBar @handleTab="handleTabApp" />
  </div>
</template>


<script>
import One from "./components/one";
import Two from "./components/two";
import Three from "./components/three";
import Four from "./components/four";
import TabBar from "./components/tabBar";
export default {
  data() {
    return {
      elect: "One"
    };
  },
  components: {
    One,
    Two,
    Three,
    Four,
    TabBar,
  },
  methods: {
    handleTabApp(index) {
      switch (index) {
        case 0:
          this.elect = "One";
          break;
        case 1:
          this.elect = "Two";
          break;
        case 2:
          this.elect = "Three";
          break;
        case 3:
          this.elect = "Four";
          break;
      }
    }
  }
};
</script>

<style>
#app {
  height: 100%;
}
.page {
  width: 100%;
  position: absolute;
  top: 0;
  bottom: 0;
  padding-top: 1.5rem;
  padding-bottom: 1.5rem;
}
</style>
