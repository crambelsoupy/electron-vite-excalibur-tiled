<script setup lang="ts">
import { game } from "./game"
import { Resources, loader } from './resources';
const ipcHandle = () => window.electron.ipcRenderer.send('ping')
game.start(loader).then(() => Resources.TiledMap.addToScene(game.currentScene));
</script>

<template>
</template>
