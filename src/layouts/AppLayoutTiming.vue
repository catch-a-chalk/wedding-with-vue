<template>
  <section id="timing">
    <h2 class="visually-hidden">Тайминг мероприятия</h2>
    <img class="heading" src="../assets/images/TIMING.svg" alt="Тайминг"/>
    <div class="wrapper">
      <ul>
        <li>
          <p>11:30</p>
          <span>Роспись в загсе</span>
        </li>
        <li>
          <p>15:30</p>
          <span>Велком-зона для гостей</span>
        </li>
        <li>
          <p>16:00</p>
          <span>Банкет</span>
        </li>
        <li>
          <p>21:00</p>
          <span>Торт</span>
        </li>
        <li>
          <p>22:00</p>
          <span>Закрытие мероприятия</span>
        </li>
      </ul>
    </div>
  </section>
</template>

<script setup></script>

<style lang="scss" scoped>
section {
  background-color: #8F979C;
}

.heading {
  width: 155px;
}

ul {
  width: fit-content;
  list-style: none;
  display: flex;
  flex-direction: column;
  margin: 0;
  padding: 0;
}

li {
  width: fit-content;
  display: flex;
  flex-direction: row;
  gap: 17px;
  align-items: baseline;
  justify-items: baseline;
}

p,
span {
  color: #151515;
}

p {
  font-size: 32px;
  line-height: 54px;
  font-style: italic;
  margin: 0;
}

@media(min-width: 768px) {
  section {
    padding-bottom: 35px;
  }

  .heading {
    width: 308px;
  }

  li {
    grid-template-columns: 1fr 4fr;
  }

  p {
    font-size: 48px;
    line-height: 81px;
  }

  span {
    font-size: 25px;
    line-height: 81px;
  }
}
</style>