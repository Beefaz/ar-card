<template>
  <a-scene
      embedded
      arjs="sourceType: webcam; debugUIEnabled: false;"
      style="height: 100%; width: 100%;"
  >
    <a-assets>
      <a-asset-item id="teapot-model" src="https://dainty-choux-81d08f.netlify.app/public/Card.gltf"></a-asset-item>
    </a-assets>

    <a-marker preset="custom" type="pattern" url="./assets/marker.patt">
      <a-entity
          gltf-model="#teapot-model"
          scale="0.01 0.01 0.01"
          position="0 0 0"
      ></a-entity>
    </a-marker>

    <a-entity camera></a-entity>
  </a-scene>
</template>

<script>
export default {
  mounted() {
    // Set the camera position and rotation
    const camera = document.querySelector("[camera]");
    camera.setAttribute("position", "0 0 0");
    camera.setAttribute("rotation", "0 0 0");
  },
};
</script>
