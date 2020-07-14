<template>
  <home-section id="regulamin" title="Regulamin" class="terms">
    <ol class="terms__list">
      <li class="terms__element">
        Doba zakwaterowania trwa od 16:00 do 10:00. Wcześniejszy przyjazd i
        późnieszy wyjazd należy uzgodnić z właścicielem.
      </li>
      <li class="terms__element">
        W dniu przyjazdu należy dokonać fromalości meldunkowych, wpłacić
        należność za pobyt oraz uiścić opłatę klimatyczną.
      </li>
      <li class="terms__element">
        Na terenie obiektu obowiązuje cisza nocna od 22:00 do 7:00.
      </li>
      <li class="terms__element">
        We wszystkich pomieszczeniach obowiązuje zakaz palenia wyrobów
        tytoniowych.
      </li>
      <li class="terms__element">
        Właściciel obiektu nie odpowiada za rzeczy zaginione lub pozostwione w
        pokojach.
      </li>
      <li class="terms__element">
        Wszelkie usterki zauważone w pokojach i łazienkach prosimy niezwłocznie
        zgłaszać właścicielowi.
      </li>
      <li class="terms__element">
        Jeżeli w trakcie pobytu nastąpiło zniszczenie elementów wyposażenia
        pokoju lub łazienki, w dniu wyjazdu podlega zapłacie.
      </li>
      <li class="terms__element">
        Miejsce przeznaczone do parkowania samochodów nie jest parkingiem
        strzeżonym.
      </li>
      <li class="terms__element">
        W czasie burzy prosimy o wyłączenie odbiornika tv z gniazdka
        elektrycznego i antenowego.
      </li>
    </ol>
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
.terms {
  &__element {
    margin-bottom: 1rem;

    &:last-of-type {
      margin-bottom: 0;
    }

    &:hover {
      background-color: rgb(238, 238, 238);
    }
  }
}
</style>
