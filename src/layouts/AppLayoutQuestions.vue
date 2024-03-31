<template>
  <section id="questions">
    <img class="heading" src="../assets/images/QUESTIONS.svg" alt="Вопросы"/>
    <ul>
      <li>
        <h3 class="subheader">Присутствие в загсе доступно для всех?</h3>
        <p class="paragraph">&mdash;&nbsp;К&nbsp;сожалению, нет. Вместимость зала не&nbsp;позволяет нам разместить всех желающих, но&nbsp;не&nbsp;расстраивайтесь! На&nbsp;велкоме будет выездная регистрация, так что просим быть вовремя :&#41;</p>
      </li>
      <li>
        <h3 class="subheader">Как добраться до места празднования?</h3>
        <p class="paragraph">&mdash;&nbsp;Можно и&nbsp;на&nbsp;личном, и&nbsp;на&nbsp;общественном транспорте. Для гостей будет доступна парковка на&nbsp;заднем дворе, а&nbsp;путь от&nbsp;метро до&nbsp;места займет не&nbsp;более 5&nbsp;минут</p>
        <iframe :src="mapIframeSrc" :height="iframeHeight" width="100%" frameborder="0"></iframe>
      </li>
      <li>
        <h3 class="subheader">А если хотим подарить цветы?</h3>
        <p class="paragraph">&mdash;&nbsp;Так как мы&nbsp;через день улетаем в&nbsp;свадебное путешествие, то&nbsp;и&nbsp;времени насладиться ароматами Ваших букетов у&nbsp;нас не&nbsp;хватит. Вместо этого можно оставить любую сумму на&nbsp;цветочную подписку по&nbsp;кнопке ниже</p>
        <a href="https://api.whatsapp.com/send?phone=79299170599&text=ODWEDDING%20%D0%9F%D0%BE%D0%B6%D0%B0%D0%BB%D1%83%D0%B9%D1%81%D1%82%D0%B0,%20%D0%BD%D0%B5%20%D1%81%D1%82%D0%B8%D1%80%D0%B0%D0%B9%D1%82%D0%B5%20%D1%8D%D1%82%D0%BE%20%D1%81%D0%BE%D0%BE%D0%B1%D1%89%D0%B5%D0%BD%D0%B8%D0%B5,%20%D1%82%D0%B0%D0%BA%20%D0%BC%D1%8B%20%D1%83%D0%B7%D0%BD%D0%B0%D0%B5%D0%BC,%20%D1%87%D1%82%D0%BE%20%D0%B2%D1%8B%20%D1%83%D1%87%D0%B0%D1%81%D1%82%D0%BD%D0%B8%D0%BA%20%D0%BD%D1%83%D0%B6%D0%BD%D0%BE%D0%B9%20%D1%81%D0%B2%D0%B0%D0%B4%D1%8C%D0%B1%D1%8B%20">Подарить цветы</a>
      </li>
      <li>
        <h3 class="subheader">Как оставить обратную связь?</h3>
        <p class="paragraph">&mdash;&nbsp;Всю информацию необходимую информацию&nbsp;Вы можете заполнить в&nbsp;Яндекс.Форме</p>
        <a href="https://forms.yandex.ru/u/6607fefd5056905ccde40a17/">Заполнить форму</a>
      </li>
    </ul>
  </section>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const mapIframeSrc = "https://yandex.ru/map-widget/v1/?um=constructor%3A08278916ac6050541dcc72d77d0a03f0d168c0787e9b377d0fdee4dd09a19b51&amp;source=constructor";

const iframeHeight = ref(400); // Начальная высота для десктопов

// Обновляем высоту iframe в зависимости от ширины экрана
onMounted(() => {
  updateIframeHeight();
  window.addEventListener('resize', updateIframeHeight);
});

function updateIframeHeight() {
  const screenWidth = window.innerWidth;
  if (screenWidth < 768) { // Мобильные устройства
    iframeHeight.value = 200;
  } else if (screenWidth < 1024) { // Планшеты
    iframeHeight.value = 362;
  } else { // Десктопы
    iframeHeight.value = 400;
  }
}
</script>

<style lang="scss" scoped>
section {
  background-color: #242631;
  padding-bottom: 15px;
}

.heading {
  width: 163px;
}

ul {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 30px;
  margin: 0;
  padding: 0;
}

li {
  display: flex;
  flex-direction: column;
  gap: 10px;
  align-items: center;
}

.subheader,
.paragraph {
  color: #D3D3D3;
  padding: 0 15px;
}

.subheader {
  line-height: 30px;
  margin: 0;
}

a {
  width: 216px;
  font-size: 19px;
  line-height: 30px;
  text-decoration: underline;

  color: #242631;
  background-color: #D9D9D9;
  padding: 4px 14px;
}

@media(min-width: 768px) {
  section {
    padding-bottom: 60px;
  }

  .heading {
    width: 325px;
  }

  ul {
    gap: 45px;
  }

  .subheader,
  .paragraph {
    padding: 0 30px;
}
}
</style>