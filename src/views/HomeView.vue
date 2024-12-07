<script setup>
import HomeCard from '@/components/HomeCard.vue'
</script>

<template>
  <div class="p-8 conten">
    <button type="button" class="text-white text-2xl font-semibold hover:underline cursor-pointer">
      Made For Abdelrahman
    </button>
    <div class="py-1.5"></div>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 gap-4">
      <HomeCard image="https://picsum.photos/id/30/300/300" title="Hello" subTitle="Adele" />
      <HomeCard
        image="https://picsum.photos/id/35/300/300"
        title="Shape of You"
        subTitle="Ed Sheeran"
      />
      <HomeCard
        image="https://picsum.photos/id/40/300/300"
        title="Blinding Lights"
        subTitle="The Weeknd"
      />
      <HomeCard image="https://picsum.photos/id/99/300/300" title="Someone Like" subTitle="Adele" />
      <HomeCard image="https://picsum.photos/id/55/300/300" title="Perfect" subTitle="Ed Sheeran" />
    </div>
  </div>
  <div class="conten">
    <button type="button" class="text-white text-2xl font-semibold hover:underline cursor-pointer">
      Recently played
    </button>
    <div class="py-1.5"></div>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 gap-4">
      <HomeCard
        image="https://picsum.photos/id/20/300/300"
        title="Havana"
        subTitle="Camila Cabello"
      />
      <HomeCard image="https://picsum.photos/id/25/300/300" title="Rolling in" subTitle="Adele" />
      <HomeCard
        class="md:block hidden"
        image="https://picsum.photos/id/50/300/300"
        title="Believer"
        subTitle="Imagine Dragons"
      />
      <HomeCard
        class="lg:block hidden"
        image="https://picsum.photos/id/200/300/300"
        title="Shallow"
        subTitle="Lady Gaga"
      />
      <HomeCard
        class="xl:block hidden"
        image="https://picsum.photos/id/65/300/300"
        title="Memories"
        subTitle="Maroon 5"
      />
    </div>
  </div>
  <div class="conten">
    <button type="button" class="text-white text-2xl font-semibold hover:underline cursor-pointer">
      Podcasts to make you smarter
    </button>
    <div class="py-1.5"></div>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 gap-4">
      <HomeCard image="https://picsum.photos/id/10/300/300" title="Fix You" subTitle="Coldplay" />
      <HomeCard
        image="https://picsum.photos/id/15/300/300"
        title="Let It Be"
        subTitle="The Beatles"
      />
      <HomeCard
        class="md:block hidden"
        image="https://picsum.photos/id/70/300/300"
        title="Yesterday"
        subTitle="The Beatles"
      />
      <HomeCard
        class="lg:block hidden"
        image="https://picsum.photos/id/75/300/300"
        title="Imagine"
        subTitle="John Lennon"
      />
      <HomeCard
        class="xl:block hidden"
        image="https://picsum.photos/id/80/300/300"
        title="Radioactive"
        subTitle="Imagine Dragons"
      />
    </div>
  </div>
  <div class="conten">
    <button type="button" class="text-white text-2xl font-semibold hover:underline cursor-pointer">
      Recommended songs
    </button>
    <div class="py-1.5"></div>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 gap-4">
      <HomeCard image="https://picsum.photos/id/81/300/300" title="Stay" subTitle="Justin Bieber" />
      <HomeCard
        image="https://picsum.photos/id/35/300/300"
        title="Bad Guy"
        subTitle="Billie Eilish"
      />
      <HomeCard
        class="md:block hidden"
        image="https://picsum.photos/id/82/300/300"
        title="Peaches"
        subTitle="Justin Bieber"
      />
      <HomeCard
        class="lg:block hidden"
        image="https://picsum.photos/id/83/300/300"
        title="Lovely"
        subTitle="Billie Eilish"
      />
      <HomeCard
        class="xl:block hidden"
        image="https://picsum.photos/id/90/300/300"
        title="Dance Monkey"
        subTitle="Tones and I"
      />
    </div>
  </div>
  <div class="conten">
    <button type="button" class="text-white text-2xl font-semibold hover:underline cursor-pointer">
      Recommended for today
    </button>
    <div class="py-1.5"></div>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 gap-4">
      <HomeCard
        image="https://picsum.photos/id/100/300/300"
        title="Happy"
        subTitle="Pharrell Williams"
      />
      <HomeCard image="https://picsum.photos/id/106/300/300" title="Faded" subTitle="Alan Walker" />
      <HomeCard
        class="md:block hidden"
        image="https://picsum.photos/id/140/300/300"
        title="Señorita"
        subTitle="Shawn Mendes"
      />
      <HomeCard
        class="lg:block hidden"
        image="https://picsum.photos/id/145/300/300"
        title="Stay"
        subTitle="The Kid LAROI"
      />
      <HomeCard
        class="xl:block hidden"
        image="https://picsum.photos/id/155/300/300"
        title="Savage Love"
        subTitle="Jason Derulo"
      />
    </div>
  </div>
</template>

<style scoped>
@media (max-width: 750px) {
  .conten {
    padding: 7px;
  }
  .text-2xl {
    font-size: 1.2rem;
    line-height: 2rem;
  }
}
</style>
