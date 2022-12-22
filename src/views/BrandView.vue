<template>
  <section class="brand">
    <BrandHeader />
    <section class="brand-second">
      <div class="container">
        <p class="text-prime mb-40">Go Ahead — экосистема сервисов и технологий digital-маркетинга. <br />
          Группа компаний включает в себя:</p>
        <div class="brand-second-list">
          <div class="brand-second-card" v-for="i in list" :key="i.id">
            <div class="brand-card__logo">
              <img :src="getImgUrl(i.id)" alt="logo" class="brand-card__logo-img">
              <div class="brand-card__logo-title"><span :style="{ color: i.logo }">go</span>{{ i.title }}</div>
            </div>
            <p class="brand-second-card__title text-second">
              {{ i.subtitle }}
            </p>
          </div>
        </div>
        <p class="text-prime mb-40">Во всех визуальных материалах о Go Ahead в качестве компаний, входящих в группу,
          указываем
          вышеуказанные 5 брендов. К таким материалам могут относиться обложки для соцсетей, слайды презентаций,
          видеовизитка.</p>
        <p class="text-prime">Для маркетинговых задач мы можем ситуативно прибегать к упоминаниям других юнитов с
          приставкой «Go». Важно понимать, что полноценными компаниями они не являются и не фигурируют на визуальных
          материалах Go Ahead общего характера. К таким юнитам/продуктам можно отнести Go ASO, Go Consulting, Go Awards,
          Go :nnection и т д.</p>
      </div>
    </section>

  </section>
</template>

<script>
import BrandHeader from '@/components/BrandHeader.vue'
export default {
  name: 'HomeView',
  components: {
    BrandHeader,
  },
  data() {
    return {
      facebookColor: "#FC2E71",
      list: [{
        id: 1,
        title: 'mobile',
        subtitle: 'Go Mobile — агентство digital-маркетинга',
        logo: '#EF5600'
      },
      {
        id: 2,
        title: 'net',
        subtitle: 'Go NET — programmatic-платформа',
        logo: '#FC2E71'
      },
      {
        id: 3,
        title: 'predicts',
        subtitle: 'Go Predicts — технология привлечения трафика с оптимизацией на предиктивные события',
        logo: '#C873FF'
      },
      {
        id: 4,
        title: 'influence',
        subtitle: 'Go Influence — агентство influencer-маркетинга полного цикла',
        logo: '#FFA3EB'
      },
      {
        id: 5,
        title: 'design',
        subtitle: 'Go Design — дизайн-студия со специализацией на креативах для performance-маркетинга',
        logo: '#0053F1'
      }]
    }
  },
  methods: {
    getImgUrl(id) {
      var images = require.context('@/assets/img/logos/', false, /\.svg$/)
      return images('./' + id + ".svg")
    }
  },
}
</script>
<style lang="scss">
@use '@/assets/scss/abstracts' as *;

.brand-second {
  padding: 100px 0;

  &-list {
    @include flex(row, center, center);
    flex-wrap: wrap;
    gap: 16px;
    margin-bottom: 60px;
  }

  &-card {
    max-width: 403px;
    width: 100%;
    min-height: 322px;
    border: 1px solid $black;
    background: $white;
    @include flex(column, start, center);
    text-align: center;
    padding:54px 30px 0;
  }

}

.brand-card__logo {
  @include flex(column, center, center);
  margin-bottom: 30px;

  &-img {
    max-width: 91px;
    width: 100%;
  }

  &-title {
    font-weight: 700;
    font-size: 29.828px;
    line-height: 36px;
    text-align: center;
    color: $black;
    margin-top: 8px;

    span {
      color: $orange;
    }
  }
}
</style>