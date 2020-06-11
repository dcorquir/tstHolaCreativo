<template>
  <div class="gray">
    <!-- #initalBarDiv -->
    <b-row>
      <HeaderComponent v-if="!isMobile()" />
      <MHeaderComponent v-if="isMobile()" />
    </b-row>
    <!-- #endInitalBarDiv -->

    <!-- #proyect -->
    <div>
      <ProyectComponent v-if="!isMobile()" />
      <MProyectComponent v-if="isMobile()" />
    </div>
    <!-- #endProyect -->
    <!-- #zoneCommond -->
    <div>
      <ZoneCommondComponent v-if="!isMobile()" />
      <MZoneCommondComponent v-if="isMobile()" />
    </div>
    <!-- #endZoneCommond -->
    <!-- #carousel -->
    <div>
      <CarouselComponent />
    </div>
    <!-- #endCarousel -->
    <!-- #zoneInterest -->
    <div>
      <ZoneInterestComponent v-if="!isMobile()" />
      <MZoneInterestComponent v-if="isMobile()" />
    </div>
    <!-- #endZoneInterest -->
    <!-- #contact -->
    <div>
      <ContactUsComponent v-if="!isMobile()" />
      <MContactUsComponent v-if="isMobile()" />
    </div>
    <!-- #endContact -->
    <!-- #map -->
    <div>
      <MapComponent v-if="!isMobile()" />
      <MMapComponent v-if="isMobile()" />
    </div>
    <!-- #endMap -->
    <!-- #group -->
    <div style="background-color: #fffffff;">
      <ProfessionalGroupComponent v-if="!isMobile()" />
      <MProfessionalGroupComponent v-if="isMobile()" />
    </div>
    <!-- #endGroup -->
    <!-- #footer -->
    <div>
      <FooterComponent v-if="!isMobile()" />
      <MFooterComponent v-if="isMobile()" />
    </div>
    <!-- #endFooter -->
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

// Web Components
import HeaderComponent from '../components/web/HeaderComponent';
import ProyectComponent from '../components/web/ProyectComponent';
import ZoneCommondComponent from '../components/web/ZoneCommondComponent';
import CarouselComponent from '../components/web/CarouselComponent';
import ZoneInterestComponent from '../components/web/ZoneInterestComponent';
import ContactUsComponent from '../components/web/ContactUsComponent';
import MapComponent from '../components/web/MapComponent';
import ProfessionalGroupComponent from '../components/web/PorfessionalGroupComponent';
import FooterComponent from '../components/web/FooterComponent';

// Mobile Components
import MHeaderComponent from '../components/mobile/mHeaderComponent';
import MProyectComponent from '../components/mobile/mProyectComponent';
import MZoneCommondComponent from '../components/mobile/mZoneCommondComponent';
import MZoneInterestComponent from '../components/mobile/mZoneInterestComponent';
import MContactUsComponent from '../components/mobile/mContactUsComponent';
import MMapComponent from '../components/mobile/mMapComponent';
import MProfessionalGroupComponent from '../components/mobile/mProfessionalGroupComponent';
import MFooterComponent from '../components/mobile/mFooterComponent';

export default Vue.extend({
  name: 'PageIndex',
  components: {
    // Web components
    HeaderComponent,
    ProyectComponent,
    ZoneCommondComponent,
    CarouselComponent,
    ZoneInterestComponent,
    ContactUsComponent,
    MapComponent,
    ProfessionalGroupComponent,
    FooterComponent,
    // Mobile components
    MHeaderComponent,
    MProyectComponent,
    MZoneCommondComponent,
    MZoneInterestComponent,
    MContactUsComponent,
    MMapComponent,
    MProfessionalGroupComponent,
    MFooterComponent
  },
  data () {
    return {}
  },
  methods: {
    getImgUrl (pic: string) {
      return require('../assets/' + pic)
    },
    isMobile () {
      if (/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
        console.log('ismobile')
        return true
      } else {
        console.log('isNOTmobile')
        return false
      }
    }
  }
})
</script>

<style>

.gray {
  background-color: rgb(245, 245, 245) !important;
}

.colNoPadding {
  padding-right: 0px !important;
  padding-left: 0px !important;
}

#linksMenu {
  text-align: center;
  padding-top: 1%;
  color: #ffffff;
}

.linkWite {
  color: #ffffff;
}

.linkWite:hover {
  color: #b25d31;
}

.navbar {
  background-color: rgb(70, 32, 13) !important;
  color: #ffffff !important;
}

.nav-link {
  color: #ffffff !important;
}

#nav-collapse {
  margin-left: 32%;
}

.initalBannerImage {
  background-image: url('~assets/cuts/Remanso-06.png');
  background-size: cover;
  background-repeat: no-repeat;
  min-height: 100%;
}

#imgPublOne {
  width: 50%;
  margin-top: 15%;
}

.alignRigth {
  text-align: right;
}

#formSendMail {
  background-image: url('~assets/cuts/Remanso-08.png');
  background-repeat: no-repeat;
  background-size: 100%;

  margin-top: 15%;
  max-width: 50%;
  padding: 8% 5% 5% 5%;
  text-align: center;
}

.q-field__control {
  color: #46200D;
  margin-bottom: 2px;
}

#sendTermsInfo {
  color: #ffffff;
  font-size: 9px;
}

#sendBtn {
  background: #46200D;
}

.spanTitle {
  background: rgb(231, 231, 231);
  max-width: 30%;
  padding: 1% 2% 1% 2%;
  border-radius: 10px 0px 10px 0px;
  text-align: center;
}

.mspanTitle {
  background: rgb(231, 231, 231);
  max-width: 40%;
  padding: 1% 2% 1% 2%;
  border-radius: 10px 0px 10px 0px;
  text-align: center;
}

.spanTitle-second {
  background: rgb(231, 231, 231);
  padding: 1% 2% 1% 2%;
  border-radius: 10px 0px 10px 0px;
}

.mspanTitle-second {
  background: rgb(231, 231, 231);
  padding: 1% 2% 1% 2%;
  border-radius: 10px 0px 10px 0px;
}

.spanTitle-orange {
  background: rgb(200, 91, 48);
  padding: 4% 4% 4% 4%;
  border-radius: 10px 0px 10px 0px;
  color:  rgb(70, 32, 13);
}

.mspanTitle-orange {
  background: rgb(200, 91, 48);
  padding: 4% 4% 4% 14%;
  border-radius: 10px 0px 10px 0px;
  color:  rgb(70, 32, 13);
}

#sectionProject {
  padding: 5% 5% 5% 5%;
}

.contatUs {
  background-image: url('~assets/cuts/Remanso-27.png');
  background-repeat: no-repeat;
  background-size: 100%;
  text-align: center;
  color: #ffffff;
  padding: 0% 0% 1% 0%;
}

.mcontatUs {
  background-image: url('~assets/cuts/Remanso-27.png');
  background-repeat: no-repeat;
}

.footer {
  background-image: url('~assets/cuts/Remanso-36.png');
  background-repeat: no-repeat;
  background-size: 100%;
  text-align: center;
  color: rgb(70, 32, 13);
}

.mfooter {
  background-image: url('~assets/cuts/Remanso-36.png');
  background-repeat: no-repeat;
  text-align: center;
  color: rgb(70, 32, 13);
}

.mheaderheigth {
  min-height: 20rem;
}

</style>
