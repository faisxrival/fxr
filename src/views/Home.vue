<template>
  <div class="home">
    <HeaderFxr />
    <HeroFxr />
    <WomenFxr />
    <InstaFxr />
    <PartnerFxr />
    <FooterFxr />
  </div>
</template>

<script>
// @ is an alias to /src
//import HelloWorld from '@/components/HelloWorld.vue'
import HeaderFxr from '@/components/HeaderFxr.vue';
import HeroFxr from '@/components/HeroFxr.vue';
import WomenFxr from '@/components/WomenFxr.vue';
import InstaFxr from '@/components/InstaFxr.vue';
import PartnerFxr from '@/components/PartnerFxr.vue';
import FooterFxr from '@/components/FooterFxr.vue';


export default {
  name: 'Home',
  components: {
    HeaderFxr,
    HeroFxr,
    WomenFxr,
    InstaFxr,
    PartnerFxr,
    FooterFxr
  }
}
</script>
