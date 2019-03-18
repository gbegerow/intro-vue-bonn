
<template>
  <div class="clock">{{ time }}</div>
</template>

<script>
export default {
  data() {
    return {
      time: ""
    };
  },
  methods: {
    setClock: function(params) {
      this.time = new Date().toLocaleTimeString("de");
    }
  },
  mounted: function() {
    console.log("Hello from component");
    this.setClock();
    window.setInterval(() => {
      this.setClock();
    }, 1000);
  }
};
</script>

<style scoped>
.clock {
  font-family: fantasy;
  font-size: 300%;
}
</style>
