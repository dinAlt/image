<template>
  <div class="container">
    <nuxt-image
      v-for="(image, i) in [...images, ...images, ...images, ...images, ...images]"
      :key="'img-' + i"
      :src="image.src"
      :format="image.format"
      :alt="image.alt"
      class="image"
      sets="320"
    />
  </div>
</template>

<script>
export default {
  asyncData () {
    return {
      images: [
        { src: 'cloudinary:/remote/nuxt-org/blog/going-full-static/main.png', alt: 'Cloudinary' },
        { src: 'fastly:/image.jpg', alt: 'fastify' },
        { src: 'imgix:/examples/bluehat.jpg', alt: 'imgix' },
        // { src: 'https://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/Aconcagua2016.jpg/600px-Aconcagua2016.jpg', alt: 'Aconcagua Argentina' },
        { src: '/images/2000px-Everest_kalapatthar.jpg', alt: 'Mount Everest Nepal' },
        { src: '/images/2000px-Mont-Blanc_from_Planpraz_station.jpg', alt: 'Mount Kilimanjaro Tanzania' },
        { src: '/images/2000px-Mount_Vinson_from_NW_at_Vinson_Plateau_by_Christian_Stangl.jpg', alt: 'Vinson Massif Antarctic' },
        { src: '/images/2000px-Wonder_Lake_and_Denali.jpg', alt: 'Denali Alaska' },
        { src: '/images/1280px-K2_2006b.jpg', alt: 'K2' },
        { src: '/images/damavand.jpg', alt: 'Damavand' },
        { src: '/images/1280px-ChoOyu-fromGokyo.jpg', alt: 'Cho Oyu' },
        { src: 'twicpics:/v1/placeholder:200x100:medium-violet-red', alt: 'Placeholder', format: 'jpg' }
      ]
    }
  }
}
</script>

<style scoped>
.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
</style>
