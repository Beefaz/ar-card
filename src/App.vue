<template>
  <div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
    }
  },
  created() {
    // Set the camera position and rotation
    const marker = document.querySelector("a-marker");
    marker.addEventListener ('markerFound', function () {
      if(marker.object3D.visible === true){
        const model = document.querySelector("a-entity");
        model.setAttribute("animation-mixer", "")
      }
    });
  },
};
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: rgba(255,0,0, 1);
  display: flex;
  justify-content: center;
  align-items: center;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
</style>
