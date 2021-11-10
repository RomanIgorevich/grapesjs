<template>
  <div id="gjs">
    <h1>Hello World Component!</h1>
  </div>
</template>

<script>
import grapesjs from "grapesjs";
// import greapejspreset from "grapesjs-preset-webpage";
export default {
  data() {
    return {
      editor: null,
    };
  },

  mounted() {
    this.editor = grapesjs.init({
      // Indicate where to init the editor. You can also pass an HTMLElement
      container: "#gjs",
      // Get the content for the canvas directly from the element
      // As an alternative we could use: `components: '<h1>Hello World Component!</h1>'`,
      fromElement: true,
      // Size of the editor
      height: "1000px",
      width: "auto",
      // Disable the storage manager for the moment
      storageManager: false,
      // Avoid any default panel
      panels: { defaults: [] },
    });
  },
};
</script>

<style>
/* Let's highlight canvas boundaries */
#gjs {
  border: 3px solid rgb(163, 2, 2);
}

/* Reset some default styling */
.gjs-cv-canvas {
  top: 0;
  width: 100%;
  height: 100%;
}
</style>
