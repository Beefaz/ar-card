<template>
  <div v-if="mounted">
    <a-scene vr-mode-ui="enabled: false;" loading-screen="enabled: false;" renderer="logarithmicDepthBuffer: true;"
             arjs="trackingMethod: best; sourceType: webcam; debugUIEnabled: false;" id="scene" embedded=""
             gesture-detector="" inspector="" keyboard-shortcuts="" screenshot="" device-orientation-permission-ui="">
      <a-assets>
        <a-asset-item id="animated-asset" src="assets/untitled.gltf"></a-asset-item>
      </a-assets>

      <a-marker-camera id="animated-marker" type="pattern" preset="custom" url="assets/marker.patt"
                       raycaster="objects: .clickable" emitevents="true" cursor="fuse: false; rayOrigin: mouse;">
        <a-entity id="bowser-model" animation-mixer="loop: repeat"
                  class="clickable" gesture-handler="" gltf-model="#animated-asset"
                  scale="0.3596762464186923 0.3596762464186923 0.3596762464186923"></a-entity>
      </a-marker-camera>

      <canvas class="a-canvas" data-aframe-canvas="true" width="330" height="165"></canvas>
    </a-scene>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      mounted: false,
    }
  },
  mounted() {
    // Set the camera position and rotation
    // const camera = document.querySelector("[camera]");
    // camera.setAttribute("position", "0 0 0");
    // camera.setAttribute("rotation", "0 0 0");
    this.mounted = true;
  },
};
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
