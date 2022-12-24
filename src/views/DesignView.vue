<template>
  <section class="design-first">
    <DesignHeader />
  </section>
  <section class="design-second">
    <div class="container">
      <DesignLogo/>
    </div>
  </section>
  <section class="design-third">
    <div class="container">
      <DesignUnits/>
    </div>
    
  </section>
  <section class="design-forth">
    <div class="container">
      <DesignColorList/>
    </div>
  </section>
</template>

<script>
// @ is an alias to /src
import DesignHeader from '@/components/DesignHeader.vue'
import DesignLogo from '@/components/design/DesignLogo.vue'
import DesignUnits from '@/components/design/DesignUnits.vue'
import DesignColorList from '@/components/design/DesignColorList.vue'

export default {
  name: 'HomeView',
  components: {
    DesignHeader,DesignLogo,DesignUnits,DesignColorList
  }
}
</script>
