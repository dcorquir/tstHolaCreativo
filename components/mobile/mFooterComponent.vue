<template>
  <div class="mfooter">
    <b-row>
      <b-col style="text-align: center;">
        <div class="my-3">
          <h3>SALA DE NEGOCIOS</h3>
        </div>
      </b-col>
    </b-row>
    <b-row>
      <b-col v-for="item in iconsContacts" :key="item.alt">
        <div>
          <img :src="getImgUrl(item.icon)" :alt="item.alt" style="width: 30%;">
        </div>
        <div>
          <b>{{ item.text }}</b>
        </div>
        <div>
          {{ item.info }}
        </div>
      </b-col>
    </b-row>
    <b-row>
      <b-col v-for="item in iconsContactsTwo" :key="item.alt">
        <div>
          <img :src="getImgUrl(item.icon)" :alt="item.alt" style="width: 30%;">
        </div>
        <div>
          <b>{{ item.text }}</b>
        </div>
        <div>
          {{ item.info }}
        </div>
      </b-col>
    </b-row>
    <b-row>
      <b-col style="font-size: 9px;">
        <p class="my-3">
          Las imágenes utilizadas son representaciones digitales del diseño y junto con las oficinas, locales y apartamentos
          pueden variar en la construcción final. El mobiliario, electrodomésticos, gasodomésticos, acabados y demás elementos
          que aparecen en las imágenes son una representación a fin de ilustrar la utilización de los espacios y pueden diferir
          de lo entregado o no ser entregado según lo convenido en los contratos. Las áreas privadas y construidas podrán sufrir
          ajustes y quedarán finalmente determinadas en los contratos suscritos por las partes.
        </p>
      </b-col>
    </b-row>
    <b-row>
      <b-col>
        <img src="~/assets/cuts/Remanso-35.png" class="my-3" alt="Logo" style="width: 20%;">
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  name: 'MFooterComponent',
  data () {
    return {
      iconsContacts: [
        { icon: 'cuts/Remanso-31.png', alt: '31', text: 'Tel:', info: '3439241 - 3137050212' },
        { icon: 'cuts/Remanso-32.png', alt: '32', text: 'Dirección:', info: 'Calle 6 sur # 79 - 158 Medellín' }
      ],
      iconsContactsTwo: [
        { icon: 'cuts/Remanso-33.png', alt: '33', text: 'Hora de Atención:', info: '10:00 am - 5:30 pm' },
        { icon: 'cuts/Remanso-34.png', alt: '34', text: 'Correo:', info: 'remansodelrodeo@une.net.co' }
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
