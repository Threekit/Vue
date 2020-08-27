<template>
  <div class="player-el" id="player-el" />
</template>

<script>
export default {
  name: "Theekit-Player",
  props: ["initParams"],
  mounted() {
    console.log("this", this);
    window
      .threekitPlayer({
        ...this.initParams,
        el: document.getElementById("player-el"),
      })
      .then((player) => (window.player = player));
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.player-el {
  height: 500px; /* player-el must have a discretely defined height (e.g. px, vh, etc.) */
  width: 500px;
  margin: auto;
}
</style>
