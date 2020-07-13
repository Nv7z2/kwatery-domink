<template>
  <div id="app">
    <navigation />
    <router-view />
  </div>
</template>

<script>
import Navigation from '@/components/core/Navigation';

export default {
  components: {
    Navigation
  }
};
</script>

<style lang="scss">
@import './styles/base';

#app {
  min-height: 225vh;
}
</style>
