<template>
  <div class="contatUs">
    <b-row>
      <b-col />
      <b-col>
        <div class="my-4" style="padding: 5% 20% 0% 20%;">
          <h3 class="spanTitle-orange">Contáctanos</h3>
        </div>
        <div>
          <p>
            Déjanos tus datos y un asesor de nuestro proyecto se comunicará para brindarte la mejor asesoría.
          </p>
        </div>
      </b-col>
      <b-col />
    </b-row>
    <b-row style="padding: 0% 20% 0% 20%;">
      <b-col>
        <div class="my-1">
          <b-form-input
            v-model="dataSend.name"
            placeholder="Nombre*"
          />
        </div>
        <div class="my-1">
          <b-form-input
            v-model="dataSend.name"
            placeholder="Correo Electrónico*"
          />
        </div>
      </b-col>
      <b-col>
        <div class="my-1">
          <b-form-input
            v-model="dataSend.name"
            placeholder="Ciudad*"
          />
        </div>
        <div class="my-1">
          <b-form-input
            v-model="dataSend.name"
            placeholder="Teléfono*"
          />
        </div>
      </b-col>
    </b-row>
    <b-row style="padding: 0% 20% 0% 20%;">
      <b-col>
        <div>
          <b-form-textarea
            id="textarea"
            v-model="dataSend.comment"
            placeholder="Comentario*"
            no-resize
          />
        </div>
      </b-col>
    </b-row>
    <b-row class="my-1">
      <b-col />
      <b-col style="text-align: left;">
        <span id="sendTermsInfo">Al hacer clic en enviar, estás aceptando los <b>términos y condiciones.</b></span>
        <b-button id="sendBtn" text-color="white">
          Enviar
        </b-button>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  name: 'ContactUsComponent',
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
