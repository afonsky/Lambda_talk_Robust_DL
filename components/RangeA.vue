<script setup lang="ts">
import { vue3dLoader } from "vue-3d-loader"

</script>

<template>
<vue3dLoader
  :height="440"
  :filePath="['/calo_shower_back_only.glb']"
  :backgroundColor="0xffffff"
></vue3dLoader>
</template>