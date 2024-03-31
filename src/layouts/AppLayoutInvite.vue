<template>
  <section class="invite">
    <h2 class="visually-hidden">Приглашение</h2>
    <img src="../assets/images/invitation@2x.jpg" alt="Оля и Денис"/>
    <div>
      <h3 class="subheader">Дорогие гости!</h3>
      <p class="paragraph">Один день в&nbsp;этом году будет для нас особенным, и&nbsp;мы&nbsp;хотим проветси его в&nbsp;кругу друзей и&nbsp;близких. С&nbsp;большим удовольствием приглашаем Вас на&nbsp;знаменательный праздник&nbsp;&mdash; нашу свадьбу!</p>
    </div>
  </section>
</template>

<style lang="scss" scoped>
section {
  background-color: #d3d3d3;
  display: flex;
  flex-direction: column;
  padding-bottom: 15px;
}

div {
  padding: 0 15px;
}

.subheader,
.paragraph {
  color: #1E1E1E;
}

.subheader {
  margin: 17px 0;
}

@media(min-width: 768px) {
  section {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 5px;
    padding-bottom: 60px;
  }

  img {
    width: 100%;
    max-width: 100%;
}

  div {
    position: relative;
    top: 60px;
    padding: 0 30px;
  }

  .paragraph {
    text-align: end;
  }
}
</style>