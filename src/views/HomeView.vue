<template>
  <div >
    <HomeBanner/>
    <HomeWelcome/>
    <AboutBanner/>
    <FeaturedComponent/>
  </div>
</template>

<script>
import HomeBanner from '@/components/HomeBanner.vue';
import HomeWelcome from '@/components/HomeWelcome.vue';
import AboutBanner from '@/components/AboutBanner.vue';
import FeaturedComponent from '@/components/FeaturedComponent.vue';

export default {
  name: 'HomeView',
  components: {
    HomeBanner,
    HomeWelcome,
    AboutBanner,
    FeaturedComponent
  }
}
</script>
