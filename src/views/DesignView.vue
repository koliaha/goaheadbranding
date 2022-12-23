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
      3
    </div>
  </section>
  <section class="design-forth">
    <div class="container">
      4
    </div>
  </section>
</template>

<script>
// @ is an alias to /src
import DesignHeader from '@/components/DesignHeader.vue'
import DesignLogo from '@/components/design/DesignLogo.vue'

export default {
  name: 'HomeView',
  components: {
    DesignHeader,DesignLogo
  }
}
</script>
