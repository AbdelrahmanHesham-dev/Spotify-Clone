<script setup>
import CategorySelect from '@/components/CategorySelect.vue'
</script>

<template>
  <div class="p-6">
    <button type="button" class="text-white text-2xl font-semibold hover:underline cursor-pointer">
      What Do You Want To Play ?
    </button>
    <div class="py-1.5"></div>
    <div class="grid gap-6 sm:grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4">
      <CategorySelect category="Melodies" image="https://picsum.photos/id/304/300/300" />
      <CategorySelect category="Rap " image="https://picsum.photos/id/301/300/300" />
      <CategorySelect category="Songs" image="https://picsum.photos/id/302/300/300" />
      <CategorySelect category="Podcasts" image="https://picsum.photos/id/309/300/300" />
      <CategorySelect category="AudioBooks" image="https://picsum.photos/id/310/300/300" />
      <CategorySelect category="plays guitar" image="https://picsum.photos/id/305/300/300" />
      <CategorySelect category="Rap" image="https://picsum.photos/id/306/300/300" />
      <CategorySelect category="Made for you" image="https://picsum.photos/id/307/300/300" />
      <CategorySelect category="New Release" image="https://picsum.photos/id/380/300/300" />
      <CategorySelect category="Radio" image="https://picsum.photos/id/301/300/300" />
      <CategorySelect category="Songs" image="https://picsum.photos/id/302/300/300" />
      <CategorySelect category="guitar" image="https://picsum.photos/id/309/300/300" />
      <CategorySelect category="Podcasts" image="https://picsum.photos/id/206/300/300" />
      <CategorySelect category="Rap" image="https://picsum.photos/id/208/300/300" />
      <CategorySelect category="Songs" image="https://picsum.photos/id/209/300/300" />
      <CategorySelect category="Melodies" image="https://picsum.photos/id/200/300/300" />
    </div>
  </div>
</template>
