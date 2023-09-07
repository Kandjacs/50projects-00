<template>
  <section class="h-screen flex justify-center items-center mx-auto max-w-[1400px]">
    <ImageCard
      v-for="(image, index) in imageDetails"
      :key="image.title"
      :imageDetails="image"
      :imageIndex="index"
      :isImageActive="index === activeIndex"
      @click="setActiveIndex(index)"
    />
  </section>
</template>

<script>
export default {
  name: 'ExpandingCards',
  data() {
    return {
      imageDetails: [
        {
          path: require('@/assets/images/spring.jpg'),
          title: 'spring',
        },
        {
          path: require('@/assets/images/summer.jpg'),
          title: 'summer',
        },
        {
          path: require('@/assets/images/autumn.jpg'),
          title: 'autumn',
        },
        {
          path: require('@/assets/images/winter.jpg'),
          title: 'winter',
        },
        {
          path: require('@/assets/images/beach.jpg'),
          title: 'beach',
        },
        {
          path: require('@/assets/images/mountain.jpg'),
          title: 'mountain',
        },
      ],
      activeIndex: 0,
    }
  },
  methods: {
    setActiveIndex(index) {
      this.activeIndex = index
    },
  },
}
</script>

<style>
</style>
