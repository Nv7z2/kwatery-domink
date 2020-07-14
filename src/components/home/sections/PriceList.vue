<template>
  <home-section id="cennik" title="Cennik" class="price-list">
    <div class="price-list__box-wrapper">
      <div class="price-list__box">
        <h2 class="price-list__small-heading">Pokoje</h2>

        <table class="price-list__table">
          <tr>
            <th></th>
            <th>Za osobę</th>
            <th>Za dobę</th>
          </tr>
          <tr>
            <td>
              Pok nr 1 (2os)<br />
              (+ łazienka)
            </td>
            <td>60 zł/doba</td>
            <td>120 zł/doba</td>
          </tr>
          <tr>
            <td>
              Pok nr 2 (3os)<br />
              (+ łazienka)
            </td>
            <td>60 zł/doba</td>
            <td>180 zł/doba</td>
          </tr>
          <tr>
            <td>Pok nr 3 (4os)</td>
            <td>45 zł/doba</td>
            <td>135 zł/doba</td>
          </tr>
          <tr>
            <td>Pok nr 4 (4os)</td>
            <td>45 zł/doba</td>
            <td>180 zł/doba</td>
          </tr>
          <tr>
            <td>Pok nr 5 (2os)</td>
            <td>45 zł/doba</td>
            <td>90 zł/doba</td>
          </tr>
          <tr>
            <td>Pok nr 6 (1os)</td>
            <td>50 zł/doba</td>
            <td>50 zł/doba</td>
          </tr>
          <tr>
            <td>Pok nr 7 (3os)</td>
            <td>45 zł/doba</td>
            <td>135 zł/doba</td>
          </tr>
          <tr>
            <td>Pok nr 8 (3os)</td>
            <td>45 zł/doba</td>
            <td>135 zł/doba</td>
          </tr>
          <tr>
            <td>
              Parter (2os)<br />
              (+ łazienka)
            </td>
            <td>60 zł/doba</td>
            <td>120 zł/doba</td>
          </tr>
        </table>
      </div>

      <div class="price-list__box">
        <h2 class="price-list__small-heading">Informacje</h2>

        <p>
          Po dokonaniu rezerwacji, w ciągu 7 dni prosimy o wpłacenie zadatku w
          wysokości dwóch dób hotelowych.
        </p>

        <p>
          Dane do przelewu: <br />
          Nr konta: 82 1050 1764 1000 0023 1384 6376
        </p>

        <p>
          Nazwa i adres odbiorcy: <br />
          Ryszard Dominik ul. Morska 9 84-110 Dębki
        </p>

        <p>
          W tytule przelewu prosimy o podanie daty pobytu oraz numer
          zarezerwowanego pokoju/domku.
        </p>

        <p>Każda dodatkowa osoba powyżej 4 roku życia: 25zł</p>
      </div>

      <div class="price-list__box">
        <h2 class="price-list__small-heading">Domki Holenderskie</h2>

        <table class="price-list__table">
          <tr>
            <th></th>
            <th>Za dobę</th>
          </tr>
          <tr>
            <td>
              Domek nr. 1
            </td>
            <td>240 zł/doba</td>
          </tr>
          <tr>
            <td>
              Domek nr. 2
            </td>
            <td>200 zł/doba</td>
          </tr>
          <tr>
            <td>Domek nr. 3</td>
            <td>240 zł/doba</td>
          </tr>
          <tr>
            <td>Domek nr. 4</td>
            <td>200 zł/doba</td>
          </tr>
        </table>
      </div>
    </div>
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
.price-list {
  &__small-heading {
    width: 100%;
    text-align: center;
    font-size: 1.5rem;
    color: #212121;
  }

  &__box-wrapper {
    display: flex;
    flex-direction: column;

    @include mq {
      width: 100%;
      margin: 0 auto;
      flex-direction: row;
      justify-content: space-between;
    }
  }

  &__box {
    width: 100%;
    padding: 1rem;
    border-bottom: 2px solid $primary;

    &:nth-of-type(2) {
      line-height: 1.5rem;
    }

    &:last-of-type {
      border-bottom: none;
    }

    @include mq {
      display: inline-block;
      border-right: 2px solid $primary;
      border-bottom: none;

      &:nth-of-type(2) {
        padding: 1rem 3rem;
      }

      &:last-of-type {
        border-right: none;
      }
    }
  }

  &__table {
    margin: 0 auto;

    tr:hover {
      background-color: rgb(236, 236, 236);

      &:first-child {
        background-color: transparent;
      }
    }

    tr > td {
      text-align: center;
      padding: 0.5rem;

      &:nth-child(2),
      &:nth-child(3) {
        color: #444;
        font-size: 0.8rem;
      }
    }
  }
}
</style>
