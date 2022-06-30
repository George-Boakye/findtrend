<template>
  <Header />
  <SectionOne />
  <SectionTwo />
  <SectionThree />
  <SectionFour />
  <Footer />
</template>

<script>
import Header from '@/components/Header.vue'
import SectionOne from '@/components/SectionOne.vue'
import SectionTwo from '@/components/SectionTwo.vue'
import SectionThree from '@/components/SectionThree.vue'
import SectionFour from '@/components/SectionFour.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header, SectionOne, SectionTwo, SectionThree, SectionFour, Footer
  }
}
</script>

<style>
@font-face {
  font-family: "Effra";
  src: local("Effra"), url(./fonts/Effra_Std_Rg.ttf) format("truetype");
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: 'Effra', sans-serif;
}
</style>

