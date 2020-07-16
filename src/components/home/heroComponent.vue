<template>
  <div class="home__hero hero" id="start">
    <div class="hero__description">
      <h1 class="hero__heading">Pensjonat <br /><q>Kwatery Dominik</q></h1>
      <p>
        Oferujemy Państwu wynajem pokoi oraz domków holenderskich. Budynek
        położony jest w samym sercu spokojnej, letniskowej miejscowości Dębki,
        przy ulicy Morskiej 9. Od najbliższego wejścia na plażę ‘nr 19’ dzieli
        nas zaledwie 300m!
      </p>

      <a href="#contact" class="hero__contact-link">Napisz do nas!</a>
      <a
        target="_blank"
        href="https://www.facebook.com/pages/category/Hotel-Resort/Kwatery-Dominik-Pokoje-go%C5%9Bcinne-D%C4%99bki-1190097974335770/"
        class="hero__contact-link"
        ><i class="fab fa-facebook-f"></i
      ></a>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.hero {
  z-index: 1;
  height: 100vh;
  display: flex;
  position: relative;
  align-items: flex-end;
  justify-content: flex-start;
  background: url('heroImg.jpg') 70% / cover no-repeat;

  &::before {
    z-index: -1;
    content: '';
    width: 100%;
    height: 100%;
    display: block;
    position: absolute;
    background-color: rgba(#000, 0.75);
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

  @keyframes unhideHeroDescription {
    from {
      opacity: 0;
      transform: translateX(-3rem);
    }
    to {
      opacity: 1;
      transform: translateX(0);
    }
  }

  &__description {
    margin: 0 auto 1rem;
    padding: 1rem;
    background-color: rgba(#000, 0);
    // text-align: justofy;
    width: 80%;
    color: #ddd;
    animation: unhideHeroDescription 0.5s;

    p {
      font-size: 1.15rem;
    }

    @include mq {
      margin: 0 auto 3rem;
    }

    @include mq('desktop') {
      width: 40%;
      margin: 10rem;
    }
  }

  &__contact-link {
    color: #eee;
    display: inline-block;
    margin-right: 1rem;
    text-align: center;
    padding: 0.75rem;
    border-radius: 0.25rem;
    background-color: $primary;
    letter-spacing: 0.05rem;
    font-weight: bold;
    border: 2px solid transparent;
    transition: background-color 0.25s, border-color 0.15s;

    &:last-of-type {
      width: auto;
      margin-right: 0;
      background-color: #3b5998;
    }

    &:hover {
      border-color: $primary;
      background-color: transparent;
    }

    &:hover:last-of-type {
      border-color: #3b5998;
    }

    @include mq {
      width: 15rem;
    }
  }
}
</style>
