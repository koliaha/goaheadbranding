<template>
  <section class="design-first">
    <DesignHeader />
  </section>
  <section class="design-second">
    <div class="container">
      <DesignLogo />
    </div>
  </section>
  <section class="design-third">
    <div class="container">
      <DesignUnits />
    </div>
  </section>
  <section class="design-forth">
    <div class="container">
      <DesignColorList />
    </div>
  </section>
  <section class="design-fifth">
      <DesignBack />
  </section>
  <section class="design-sixth">
      <DesignTypograph />
  </section>
  <section class="design-seventh">
      <DesignPattern />
  </section>
  <section class="design-eight">
      <DesignPresentation />
  </section>
  <section class="design-ninth">
      <DesignSmm />
  </section>
  <section class="design-tenth">
      <DesignBanners />
  </section>
  <section class="design-eleven">
      <DesignImidge />
  </section>
</template>

<script>
// @ is an alias to /src
import DesignHeader from '@/components/DesignHeader.vue'
import DesignLogo from '@/components/design/DesignLogo.vue'
import DesignUnits from '@/components/design/DesignUnits.vue'
import DesignColorList from '@/components/design/DesignColorList.vue'
import DesignBack from '@/components/design/DesignBack.vue'
import DesignTypograph from '@/components/design/DesignTypograph.vue'
import DesignPattern from '@/components/design/DesignPattern.vue'
import DesignPresentation from '@/components/design/DesignPresentation.vue'
import DesignSmm from '@/components/design/DesignSmm.vue'
import DesignBanners from '@/components/design/DesignBanners.vue'
import DesignImidge from '@/components/design/DesignImidge.vue'

export default {
  name: 'HomeView',
  components: {
    DesignHeader, DesignLogo, DesignUnits, DesignColorList, DesignBack,DesignTypograph,DesignPattern,DesignPresentation,DesignSmm,DesignBanners,DesignImidge
  }
}
</script>
