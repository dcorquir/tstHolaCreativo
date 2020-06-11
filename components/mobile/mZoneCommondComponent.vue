<template>
  <div>
    <b-row>
      <b-col style="text-align: center; padding: 0% 15% 0% 15%;">
        <h3 class="mspanTitle-second">
          Zonas Comúnes
        </h3>
      </b-col>
    </b-row>
    <b-row>
      <b-col style="text-align: center;">
        <p>
          Un lugar exclusivo para brindarte a tu y a tu familia
        </p>
      </b-col>
    </b-row>
    <b-row>
      <b-col v-for="img in zonesImgOne" :key="img.alt">
        <img :src="getImgUrl(img.url)" :alt="img.alt" style="width: 100%;">
      </b-col>
    </b-row>
    <b-row class="my-3">
      <b-col v-for="img in zonesImgTwo" :key="img.alt">
        <img :src="getImgUrl(img.url)" :alt="img.alt" style="width: 100%;">
      </b-col>
    </b-row>
    <b-row class="my-3">
      <b-col v-for="img in zonesImgThree" :key="img.alt">
        <img :src="getImgUrl(img.url)" :alt="img.alt" style="width: 100%;">
      </b-col>
    </b-row>
    <b-row class="my-3">
      <b-col v-for="img in zonesImgFour" :key="img.alt">
        <img :src="getImgUrl(img.url)" :alt="img.alt" style="width: 100%;">
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  name: 'MZoneCommondComponent',
  data () {
    return {
      zonesImgOne: [
        { url: 'cuts/Remanso-10.png', alt: '10' },
        { url: 'cuts/Remanso-11.png', alt: '11' }
      ],
      zonesImgTwo: [
        { url: 'cuts/Remanso-12.png', alt: '12' },
        { url: 'cuts/Remanso-13.png', alt: '13' }
      ],
      zonesImgThree: [
        { url: 'cuts/Remanso-14.png', alt: '14' },
        { url: 'cuts/Remanso-15.png', alt: '15' }
      ],
      zonesImgFour: [
        { url: 'cuts/Remanso-16.png', alt: '16' },
        { url: 'cuts/Remanso-17.png', alt: '17' }
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
