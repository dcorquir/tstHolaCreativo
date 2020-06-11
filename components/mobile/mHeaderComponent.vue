<template>
  <b-container class="mheaderheigth minitalBannerImage">
    <b-row>
      <b-col>
        <img src="~/assets/cuts/Remanso-05.png" alt="Logo" style="width: 100%;">
      </b-col>
      <b-col style="text-align: center; padding-top: 4%;">
        <b-dropdown text="Menu" class="m-md-2" id="sendBtn">
          <b-dropdown-item>Proyecto</b-dropdown-item>
          <b-dropdown-item>Galería</b-dropdown-item>
          <b-dropdown-item>Apartamento</b-dropdown-item>
          <b-dropdown-item>Mapa</b-dropdown-item>
          <b-dropdown-item>Contacto</b-dropdown-item>
        </b-dropdown>
      </b-col>
    </b-row>
    <b-row>
      <b-col style="text-align: center;">
        <img id="mimgPublOne" src="~/assets/cuts/Remanso-07.png">
      </b-col>
    </b-row>
    <b-row>
      <b-col id="mformSendMail">
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
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: 'MHeaderComponent',
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

<style scope>
#mimgPublOne {
  width: 90%;
  margin-top: 15%;
}

.minitalBannerImage {
  background-image: url('~assets/cuts/Remanso-06.png');
  background-repeat: no-repeat;
}

.btn-secondary {
  background: #46200D;
}

#mformSendMail {
  background-image: url('~assets/cuts/Remanso-08.png');
  background-size: 83%;
  text-align: center;
  padding: 13% 15% 5% 15%;
  background-repeat: no-repeat;
  background-position-x: 50%;

}
</style>
