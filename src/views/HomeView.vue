<template>
  <div >
    <HomeBanner/>
    <HomeWelcome/>
  </div>
</template>

<script>
import HomeBanner from '@/components/HomeBanner.vue';
import HomeWelcome from '@/components/HomeWelcome.vue';

export default {
  name: 'HomeView',
  components: {
    HomeBanner,
    HomeWelcome
  }
}
</script>
