<template>
  <div class="mcontatUs">
    <b-row>
      <b-col>
        <div class="my-4" style="padding: 5% 20% 0% 20%;">
          <h3 class="mspanTitle-orange">Contáctanos</h3>
        </div>
        <div style="text-align: center;">
          <p>
            Déjanos tus datos y un asesor de nuestro proyecto se comunicará para brindarte la mejor asesoría.
          </p>
        </div>
      </b-col>
    </b-row>
    <b-row>
      <b-col style="padding: 0% 15% 10% 15%;">
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
        <div style="text-align: center;">
          <span id="sendTermsInfo">Al hacer clic en enviar, estás aceptando los <b>términos y condiciones.</b></span>
        </div>
        <div style="text-align: center;">
          <b-button id="sendBtn" text-color="white" size="sm">
            Enviar
          </b-button>
        </div>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  name: 'MContactUsComponent',
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
