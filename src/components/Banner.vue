<script setup lang="ts">

import { onMounted, ref } from 'vue';

interface Props {
  src: string
}

defineProps<Props>();

const videoPlayer = ref<HTMLVideoElement | null>(null);

onMounted(() => {
  if (videoPlayer.value) {
    videoPlayer.value.play();
  }
});

</script>

<template>
  <video ref="videoPlayer" autoplay loop muted playsinline class="w-full h-96 object-cover">
    <source :src="src">
  </video>
</template>