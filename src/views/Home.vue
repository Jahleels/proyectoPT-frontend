<template>
  <v-app>
  <header-section />
  <nosotros-section />
  <talleres-section />
  <servicios-section />
  <footer-section />
  </v-app>
</template>

<script>
import FooterSection from '../components/FooterSection.vue'
  import HeaderSection from '../components/HeaderSection'
  import NosotrosSection from '../components/NosotrosSection'
import ServiciosSection from '../components/ServiciosSection.vue'
import TalleresSection from '../components/TalleresSection.vue'
  export default {
    name: 'Home',

    components: {
        HeaderSection,
        NosotrosSection,
        TalleresSection,
        ServiciosSection,
        FooterSection
    },
  }
</script>



