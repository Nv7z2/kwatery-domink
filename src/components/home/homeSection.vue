<template>
  <section class="home__section section" :id="id">
    <h2 class="section__heading">{{ title }}</h2>

    <slot />
  </section>
</template>

<script>
export default {
  props: {
    id: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: true
    }
  }
};
</script>

<style lang="scss" scoped>
.section {
  padding: 1rem;
  scroll-margin-top: 100px;

  @include mq {
    padding: 2rem;
  }

  &__heading {
    color: rgb(97, 97, 97);
    font-size: 1.75rem;
    margin-top: 0;

    @include mq {
      font-size: 2.5rem;
    }
  }
}
</style>
