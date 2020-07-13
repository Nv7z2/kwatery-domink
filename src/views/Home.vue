<template>
  <div class="home">
    <hero-component />
  </div>
</template>

<script>
import heroComponent from '@/components/home/heroComponent';

export default {
  name: 'Home',
  components: {
    heroComponent
  }
};
</script>

<style lang="scss" scoped></style>
