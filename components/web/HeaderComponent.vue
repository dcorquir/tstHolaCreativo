<template>
  <b-col>
    <div class="initalBannerImage">
      <b-row>
        <b-col style="padding-left: 5%;">
          <img src="~/assets/cuts/Remanso-05.png" alt="Logo" style="width: 50%;">
        </b-col>
        <b-col id="linksMenu">
          <b-link class="linkWite" href="#">
            Proyecto
          </b-link>
          <b>|</b>
          <b-link class="linkWite" href="#">
            Galería
          </b-link>
          <b>|</b>
          <b-link class="linkWite" href="#">
            Apartamento
          </b-link>
          <b>|</b>
          <b-link class="linkWite" href="#">
            Mapa
          </b-link>
          <b>|</b>
          <b-link class="linkWite" href="#">
            Contacto
          </b-link>
        </b-col>
        <b-col />
      </b-row>

      <b-row>
        <b-col class="alignRigth colNoPadding">
          <img id="imgPublOne" src="~/assets/cuts/Remanso-07.png">
        </b-col>
        <b-col class="colNoPadding">
          <div id="formSendMail">
            <div class="my-1">
              <b-form-input
                v-model="dataSend.name"
                placeholder="Nombre*"
                size="sm"
              />
            </div>
            <div class="my-1">
              <b-form-input
                v-model="dataSend.name"
                placeholder="Correo Electrónico*"
                size="sm"
              />
            </div>
            <div class="my-1">
              <b-form-input
                v-model="dataSend.name"
                placeholder="Teléfono*"
                size="sm"
              />
            </div>
            <div class="my-1">
              <b-form-input
                v-model="dataSend.name"
                placeholder="Ciudad*"
                size="sm"
              />
            </div>
            <div>
              <b-form-textarea
                id="textarea"
                v-model="dataSend.comment"
                placeholder="Comentario*"
                size="sm"
                no-resize
              />
            </div>
            <div>
              <span id="sendTermsInfo">Al hacer clic en enviar, estás aceptando los <b>términos y condiciones.</b></span>
            </div>
            <div>
              <b-button id="sendBtn" text-color="white" size="sm">
                Enviar
              </b-button>
            </div>
          </div>
        </b-col>
      </b-row>
    </div>
  </b-col>
</template>

<script>
export default {
  name: 'HeaderComponent',
  data () {
    return {
      dataSend: {
        name: '',
        email: '',
        phone: '',
        city: '',
        comment: ''
      }
    }
  }
}
</script>
