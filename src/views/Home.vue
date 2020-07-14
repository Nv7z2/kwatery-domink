<template>
  <div class="home">
    <hero-component />
    <price-list />
    <contact />
    <news />
    <terms />
    <home-footer />
  </div>
</template>

<script>
import heroComponent from '@/components/home/heroComponent';
import PriceList from '@/components/home/sections/PriceList';
import Contact from '@/components/home/sections/Contact';
import News from '@/components/home/sections/News';
import Terms from '@/components/home/sections/Terms';
import HomeFooter from '@/components/home/homeFooter';

export default {
  name: 'Home',
  components: {
    heroComponent,
    PriceList,
    Contact,
    News,
    Terms,
    HomeFooter
  }
};
</script>

<style lang="scss" scoped></style>
