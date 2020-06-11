<template>
  <div>
    <b-row>
      <b-col style="text-align: center;">
        <img src="~/assets/cuts/Remanso-18.png" alt="18" style="width: 100%;">
      </b-col>
    </b-row>
    <b-row class="my-5">
      <b-col style="text-align: center;">
        <img src="~/assets/cuts/Remanso-19.png" alt="19" style="width: 100%;">
      </b-col>
    </b-row>
    <b-row class="my-3">
      <b-col v-for="img in urbZoneImgsOne" :key="img.alt">
        <img :src="getImgUrl(img.url)" :alt="img.alt" style="width: 100%;">
      </b-col>
    </b-row>
    <b-row class="my-3">
      <b-col v-for="img in urbZoneImgsTwo" :key="img.alt">
        <img :src="getImgUrl(img.url)" :alt="img.alt" style="width: 100%;">
      </b-col>
    </b-row>
    <b-row class="my-3">
      <b-col v-for="img in urbZoneImgsThree" :key="img.alt">
        <img :src="getImgUrl(img.url)" :alt="img.alt" style="width: 100%;">
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  name: 'MZoneInterestComponent',
  data () {
    return {
      urbZoneImgsOne: [
        { url: 'cuts/Remanso-21.png', alt: '21' },
        { url: 'cuts/Remanso-22.png', alt: '22' }
      ],
      urbZoneImgsTwo: [
        { url: 'cuts/Remanso-23.png', alt: '23' },
        { url: 'cuts/Remanso-24.png', alt: '24' }
      ],
      urbZoneImgsThree: [
        { url: 'cuts/Remanso-25.png', alt: '25' },
        { url: 'cuts/Remanso-26.png', alt: '26' }
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
