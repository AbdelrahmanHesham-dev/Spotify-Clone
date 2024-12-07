<script setup>
import SongRow from '../components/SongRow.vue'
import Play from 'vue-material-design-icons/Play.vue'
import Pause from 'vue-material-design-icons/Pause.vue'
import DotsHorizontal from 'vue-material-design-icons/DotsHorizontal.vue'
import Heart from 'vue-material-design-icons/Heart.vue'
import ClockTimeThreeOutline from 'vue-material-design-icons/ClockTimeThreeOutline.vue'
import artist from '../artist.json'

import { useSongStore } from '../stores/song'
import { storeToRefs } from 'pinia'
const useSong = useSongStore()
const { isPlaying, currentTrack, currentArtist } = storeToRefs(useSong)

const playFunc = () => {
  if (currentTrack.value) {
    useSong.playOrPauseThisSong(currentArtist.value, currentTrack.value)
    return
  }
  useSong.playFromFirst()
}
</script>

<template>
  <div class="p-8 conten overflow-x-hidden">
    <button type="button" class="text-white text-2xl font-semibold hover:underline cursor-pointer">
      Abdelrahman Library
    </button>
    <!-- ############################## -->
    <div class="flex items-start flex-col md:flex-row md:items-center w-full relative h-full">
      <div class="flex justify-center mt-7">
        <img class="w-[180px] md:w-[180px]" :src="artist.albumCover" />
      </div>

      <div class="w-full md:mt--10 md:ml-5">
        <div
          style="font-size: 33px"
          class="text-white hover:underline cursor-pointer font-bosemiboldld"
        >
          {{ artist.name }}
        </div>

        <div class="text-gray-300 text-[13px] flex flex-wrap md:flex-nowrap">
          <div class="py-4 flex">Album</div>
          <div class="ml-2 py-4 flex">
            <div class="circle mt-2 mr-2"></div>
            <span class="-ml-0.5">{{ artist.releaseYear }}</span>
          </div>
          <div class="ml-2 py-4 flex">
            <div class="circle mt-2 mr-2"></div>
            <span class="-ml-0.5">{{ artist.tracks.length }} songs</span>
          </div>
        </div>

        <div class="flex gap-4 items-center justify-start md:absolute">
          <button class="p-1 rounded-full bg-white" @click="playFunc()">
            <Play v-if="!isPlaying" fillColor="#181818" :size="25" />
            <Pause v-else fillColor="#181818" :size="25" />
          </button>
          <button type="button">
            <Heart fillColor="#1BD760" :size="30" />
          </button>
          <button type="button">
            <DotsHorizontal fillColor="#FFFFFF" :size="25" />
          </button>
        </div>
      </div>
    </div>

    <!-- ############################## -->
    <div class="mt-6"></div>
    <div class="flex items-center justify-between px-5 pt-2 fix">
      <div class="flex items-center justify-between text-gray-400">
        <div class="mr-7">#</div>
        <div class="text-sm">Title</div>
      </div>
      <div><ClockTimeThreeOutline fillColor="#FFFFFF" :size="18" /></div>
    </div>
    <div class="border-b border-b-[#2A2A2A] mt-2"></div>
    <div class="mb-4"></div>
    <ul class="w-full" v-for="(track, index) in artist.tracks" :key="track">
      <SongRow :artist="artist" :track="track" :index="++index" />
    </ul>
  </div>
</template>

<style scoped>
.circle {
  width: 4px;
  height: 4px;
  background-color: rgb(189, 189, 189);
  border-radius: 100%;
}
@media (max-width: 750px) {
  .conten {
    padding: 9px;
  }
  .text-2xl {
    font-size: 1.2rem;
    line-height: 2rem;
  }
  .fix {
    padding: 0;
  }
}
</style>
