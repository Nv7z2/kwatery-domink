<template>
  <div class="home__hero hero" id="start">
    <div class="hero__description">
      <h1 class="hero__heading">Pensjonat <br /><q>Kwatery Dominik</q></h1>
      <p>
        Oferujemy Państwu wynajem pokoi oraz domków holenderskich. Budynek
        położony jest w samym sercu spokojnej, letniskowej miejscowości Dębki,
        przy ulicy Morskiej 9. Od najbliższego wejścia na plażę ‘nr 19’ dzieli
        nas zaledwie 300m! Znajdziecie u nas Państwo wszystko czego potrzeba do
        wypoczynku nad morzem, zarówno aktywnego jak i tego trochę mniej ;D
      </p>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    this.backgroundParallax();
  },
  methods: {
    backgroundParallax() {
      document.addEventListener('scroll', () => {
        document.querySelector(
          '.hero'
        ).style.backgroundPositionY = `${window.scrollY / 2}px`;
      });
    }
  }
};
</script>

<style lang="scss" scoped>
.hero {
  z-index: 1;
  height: 100vh;
  display: flex;
  position: relative;
  align-items: center;
  justify-content: center;
  background: url('heroImg.jpg') 70% / cover no-repeat;

  &::before {
    z-index: -1;
    content: '';
    width: 100%;
    height: 100%;
    display: block;
    position: absolute;
    background-color: rgba(#000, 0.5);
  }

  @include mq {
    background-position: 75%;
  }

  @include mq('desktop') {
    background-position: center;
  }

  &__heading {
    color: #eee;
    margin: 0 0 1rem 0;
    font-size: 1.5rem;

    @include mq {
      font-size: 2rem;
    }
  }

  &__description {
    padding: 1rem;
    background-color: rgba(#000, 0.5);
    text-align: center;
    width: 80%;
    color: #ddd;

    p {
      font-size: 1.15rem;
    }

    @include mq {
      width: 50%;
    }
  }
}
</style>
