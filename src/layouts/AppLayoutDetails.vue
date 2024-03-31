<template>
  <section id="details">
    <h2 class="visually-hidden">Детали</h2>
    <img class="heading" src="../assets/images/DETAILS.svg" alt="Детали"/>
    <div class="wrapper">
      <ul>
        <li>
          <img class="details__icon" src="../assets/images/icons/icon-gift.svg" width="47" alt="Подарки"/>
          <h3 class="subheader">Подарки</h3>
          <p class="paragraph">Ваши пожелания в&nbsp;конвертах будут лучшим подарком, который позволит нам воплоитть наши мечты</p>
        </li>
        <li>
          <img class="details__icon" src="../assets/images/icons/icon-suit.svg" width="47" alt="Подарки"/>
          <h3 class="subheader">Дресс-код</h3>
          <p class="paragraph"><strong>ЖЕНЩИНЫ:</strong>  костюмы, юбки, блузки, вечерние платья<br><strong>МУЖЧИНЫ:</strong> брюки, рубашки, пиджаки, футболки, поло</p>
        </li>
        <li>
          <img class="details__icon" src="../assets/images/icons/icon-paint.svg" width="47" alt="Подарки"/>
          <h3 class="subheader">Цветовая гамма</h3>
          <p class="paragraph">Мы&nbsp;очень старались сделать праздник красивым и&nbsp;будем рады, если в&nbsp;своих нарядах&nbsp;Вы поддержите цветовую гамму нашей свадьбы:</p>
          <img class="details__palette" src="../assets/images/palette.svg" alt="Цветовая палитра"/>
        </li>
      </ul>
    </div>
  </section>
</template>

<style lang="scss" scoped>
section {
  background-color: #364140;
  padding-bottom: 15px;
}

.heading {
  width: 123px;
}

ul {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 30px;
  margin: 0;
  padding: 0;
}

.details__palette {
  width: 255px;
  margin-top: 10px;
}

.subheader,
.paragraph {
  color: #D3D3D3;
}

@media(min-width: 768px) {
  section {
    padding-bottom: 60px;
  }

  .heading {
    width: 243px;
  }

  ul {
    gap: 50px;
  }

  .details__icon {
    margin-top: 0;
  }

  .details__palette {
    width: 510px;
    margin-top: 20px;
  }
}
</style>