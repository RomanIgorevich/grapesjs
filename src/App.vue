<template>
  <div id="gjs">
    <h1>Hello World Component!</h1>
  </div>
</template>

<script>
import grapesjs from "grapesjs";
import "grapesjs/dist/css/grapes.min.css";

export default {
  data() {
    return {
      editor: null,
    };
  },
  mounted() {
    this.start();
  },
  methods: {
    start() {
      this.editor = grapesjs.init({
        // Указываем, где запустить редактор
        container: "#gjs",
        // Получаем содержимое холста прямо из элемента
        fromElement: true,
        // Размер редактора
        height: "300px",
        width: "auto",
        // Отключаем на время диспетчер хранилища
        storageManager: false,
        // Избегаем любой панели по умолчанию
        panels: { defaults: [] },
      });
    },
  },
};
</script>

<style>
#gjs {
  border: 3px solid #444;
}

.gjs-cv-canvas {
  top: 0;
  width: 100%;
  height: 100%;
}
</style>
