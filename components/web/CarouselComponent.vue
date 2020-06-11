<template>
  <b-row>
    <b-col>
      <b-carousel
        id="carousel-1"
        v-model="slide"
        :interval="4000"
        controls
        indicators
        background="#ababab"
        img-width="50%"
        style="text-shadow: 1px 1px 2px #333;"
      >
        <b-carousel-slide v-for="item in slideImgaes" :key="item.alt">
          <template v-slot:img>
            <img
              class="d-block img-fluid w-100"
              :src="getImgUrl(item.url)"
              :alt="item.alt"
            >
          </template>
        </b-carousel-slide>
      </b-carousel>
    </b-col>
  </b-row>
</template>

<script>
export default {
  name: 'CarouselComponent',
  data () {
    return {
      slide: 0,
      slideImgaes: [
        { url: 'galery/Remanso-41.png', alt: '41' },
        { url: 'galery/Remanso-42.png', alt: '42' },
        { url: 'galery/Remanso-43.png', alt: '43' },
        { url: 'galery/Remanso-44.png', alt: '44' },
        { url: 'galery/Remanso-45.png', alt: '45' },
        { url: 'galery/Remanso-46.png', alt: '46' },
        { url: 'galery/Remanso-47.png', alt: '47' },
        { url: 'galery/Remanso-48.png', alt: '48' },
        { url: 'galery/Remanso-49.png', alt: '49' }
      ]
    }
  },
  methods: {
    getImgUrl (pic) {
      return require('../../assets/' + pic)
    }
  }
}
</script>
