<template>
  <home-section id="aktualnosci" title="Aktualności" class="news">
    <ul class="news__list">
      <li class="news__element">
        W związku z obowiązującymi obostrzeniami odnośnie użytkowania
        przestrzeni ogólnodostępnych plac zabaw oraz kuchnia jest niedostępna do
        odwołania.
      </li>
    </ul>
  </home-section>
</template>

<script>
import homeSection from '../homeSection';

export default {
  components: {
    homeSection
  }
};
</script>

<style lang="scss" scoped>
.news {
  &__list {
    margin-left: 1rem;
    list-style: circle;
  }
}
</style>
