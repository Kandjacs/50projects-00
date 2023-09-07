<template>
  <div class="relative text-white mx-4 cursor-pointer">
    <img
      :src="imageDetails.path"
      :alt="imageIndex"
      class="h-[80vh] rounded-[4rem] object-cover transition-width duration-700 ease-in-out "
      :class="{ 'w-[50vw]': isImageActive, 'w-[10vw]': !isImageActive }"
      @click="$emit('click')"
    />
    <h1 class="absolute bottom-10 left-10 text-4xl capitalize transition-opacity duration-300 ease-in-out " :class="{'delay-100 opacity-100': isImageActive, 'opacity-0': !isImageActive}">{{ imageDetails.title }}</h1>
  </div>
</template>

<script>
export default {
  name: 'ImageCard',
  data() {},
  props: {
    imageDetails: {
      type: Object,
      required: true,
    },
    imageIndex: {
      type: Number,
      required: true,
    },
    isImageActive: {
      type: Boolean,
      required: true,
    },
  },
}
</script>

<style>
</style>
