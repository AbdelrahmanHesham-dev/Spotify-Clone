<script setup>
import { ref, toRefs } from 'vue'
import { RouterLink } from 'vue-router'
import uniqolor from 'uniqolor'
let randerColor = ref('')
randerColor.value = uniqolor.random()

const props = defineProps({ category: String, image: String })
const { category } = toRefs(props)
</script>

<template>
  <RouterLink to="/library">
    <div
      v-if="randerColor.color"
      :style="`background-color: ${randerColor.color}`"
      class="contrast-[2] brightness-[0.87] rounded-xl aspect-square relative overflow-hidden"
    >
      <div class="text-white pt-3 pl-3 font-semibold text=[23px]">{{ category }}</div>
      <img
        :src="image || ''"
        class="absolute contrast-[0.55] -right-3.5 bottom-0 rotate-[9deg] lg:max-w-[190px] md:max-w-[150px] max-w-[150px]"

        alt=""
      />
    </div>
  </RouterLink>
</template>
