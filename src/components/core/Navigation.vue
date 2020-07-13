<template>
  <nav class="navigation" :class="{ 'navigation--scrolled': isNavScrolled }">
    <img src="./logo.png" alt="" class="navigation__logo" />

    <button
      class="navigation__hamburger"
      :class="{ 'navigation__hamburger--active': isMenuActive }"
      @click="isMenuActive = !isMenuActive"
    >
      <span class="navigation__hamburger-line"></span>
      <span class="navigation__hamburger-line"></span>
      <span class="navigation__hamburger-line"></span>
    </button>

    <ul
      class="navigation__menu"
      :class="{ 'navigation__menu--active': isMenuActive }"
    >
      <li class="navigation__element">
        <a href="#" class="navigation__link">Start</a>
      </li>
      <li class="navigation__element">
        <a href="#" class="navigation__link">Cennik</a>
      </li>
      <li class="navigation__element">
        <a href="#" class="navigation__link">Galeria</a>
      </li>
      <li class="navigation__element">
        <a href="#" class="navigation__link">Kontakt</a>
      </li>
      <li class="navigation__element">
        <a href="#" class="navigation__link">Aktualności</a>
      </li>
      <li class="navigation__element">
        <a href="#" class="navigation__link">Regulamin</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      isNavScrolled: false,
      isMenuActive: false
    };
  },
  mounted() {
    this.navigationScrolled();
  },
  methods: {
    navigationScrolled() {
      document.addEventListener('scroll', () => {
        if (window.scrollY >= 200) this.isNavScrolled = true;
        else this.isNavScrolled = false;
      });
    },
    toggleMenu() {}
  }
};
</script>

<style lang="scss" scoped>
.navigation {
  z-index: 2;
  padding: 1rem;
  width: 100%;
  display: flex;
  position: fixed;
  align-items: center;
  justify-content: space-between;
  background-color: #111;

  @include mq {
    padding: 2rem;
    transition: background-color 0.15s ease-in-out;
    background-color: transparent;
  }

  &--scrolled {
    background-color: #111;
  }

  &__logo {
    height: 64px;
    margin: -1rem;
  }

  &__hamburger {
    width: 32px;
    height: 24px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    @include mq {
      display: none;
    }
  }

  &__hamburger-line {
    width: 100%;
    display: block;
    height: 2px;
    background-color: #eee;
    transition: transform 0.2s, opacity 0.1s;
  }

  &__hamburger--active &__hamburger-line {
    &:nth-of-type(1) {
      transform: translateY(0.65rem) rotate(45deg);
    }
    &:nth-of-type(2) {
      opacity: 0;
      transform: translateX(1rem);
    }
    &:nth-of-type(3) {
      transform: translateY(-0.65rem) rotate(-45deg);
    }
  }

  &__menu {
    position: absolute;
    right: 0;
    top: 3.5rem;
    width: 50vw;
    height: 100vh;
    background-color: #111;
    transform: translateX(50vw);
    transition: transform 0.2s ease-in-out;

    &--active {
      transform: translateX(0);
    }

    @include mq {
      top: 0;
      right: 0;
      height: auto;
      width: auto;
      position: relative;
      transform: translateX(0);
      background-color: transparent;
    }
  }

  &__element {
    @include mq {
      display: inline-block;
    }
  }

  &__link {
    color: #eee;
    display: block;
    height: 100%;
    padding: 1rem;

    @include mq {
      padding: 0.5rem 1rem;
      transition: border 0.15s;

      &:hover {
        border-bottom: 2px solid white;
      }
    }
  }
}
</style>
