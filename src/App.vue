<template>
  <a-scene embedded arjs>
    <a-marker preset="hiro">
      <!-- we use cors proxy to avoid cross-origin problems ATTENTION! you need to set up your server -->
      <a-entity
          position="1 1 1"
          scale="1 1 1"
          gltf-model="url(https://jovial-travesseiro-4fc45a.netlify.app/public/Card.gltf)"
      ></a-entity>
    </a-marker>
    <a-entity camera></a-entity>
  </a-scene>
<!--  <a-scene-->
<!--      embedded-->
<!--      arjs="sourceType: webcam; debugUIEnabled: false;"-->
<!--      style="height: 100%; width: 100%;"-->
<!--  >-->
<!--    <a-assets>-->
<!--      <a-asset-item id="teapot-model" src="https://jovial-travesseiro-4fc45a.netlify.app/public/Card.gltf"></a-asset-item>-->
<!--    </a-assets>-->

<!--    <a-marker preset="custom" type="pattern" url="https://jovial-travesseiro-4fc45a.netlify.app/public/marker.patt">-->
<!--      <a-entity-->
<!--          gltf-model="#teapot-model"-->
<!--          scale="0.01 0.01 0.01"-->
<!--          position="0 0 0"-->
<!--      ></a-entity>-->
<!--    </a-marker>-->

<!--    <a-entity camera></a-entity>-->
<!--  </a-scene>-->

</template>

<script>
export default {
  name: 'App',
  // mounted() {
  //   // Set the camera position and rotation
  //   const camera = document.querySelector("[camera]");
  //   camera.setAttribute("position", "0 0 0");
  //   camera.setAttribute("rotation", "0 0 0");
  // },
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
