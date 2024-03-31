<template>
  <section id="place-and-date">
    <h2 class="visually-hidden">Место и время</h2>
    <img class="heading" src="../assets/images/PLACE.svg" alt="Место и дата"/>
    <div class="wrapper">
      <img src="../assets/images/768-banket.jpg" alt="Фото зала"/>
      <ul>
        <li>
          <svg xmlns="http://www.w3.org/2000/svg" width="40" height="56" fill="none"><path fill="#2A2A2A" fill-rule="evenodd" d="M19.6 25.81a5.6 5.6 0 1 1 0-11.2 5.6 5.6 0 0 1 0 11.2ZM19.6 0A19.6 19.6 0 0 0 0 19.6C0 30.42 19.6 56 19.6 56s19.6-25.58 19.6-36.4A19.6 19.6 0 0 0 19.6 0Z" clip-rule="evenodd"/></svg>
          <h3 class="subheader">Локация</h3>
          <p class="paragraph">Наша свадьба пройдет в банкетном зале <strong>Ya Cafe улицы Ленинской Слободы, д. 19, стр. 2</strong></p>
        </li>
        <li>
          <svg xmlns="http://www.w3.org/2000/svg" width="52" height="56" fill="none"><path fill="#2A2A2A" fill-rule="evenodd" d="M24 4h8v3h-3v3.02c3.82.16 7.39 1.26 10.5 3.06 1.85-1.93 6.26.17 4.76 3.66l-.1-.1a23 23 0 1 1-32.43.1c-2.02-3.03 2.59-6.16 4.77-3.66 3.11-1.8 6.68-2.9 10.5-3.06V7h-3V4Z" clip-rule="evenodd"/><path fill="#C2CDCA" fill-rule="evenodd" d="M27 1h-6v1h6V1Zm-2 2h3V0h-8v3h3v3.02a22.87 22.87 0 0 0-9.6 2.57l-.15-.17c-1.53-1.76-3.85-1.44-5.3-.4a4.14 4.14 0 0 0-1.6 2.26c-.26.96-.1 2.02.56 3.01l.12.19a23 23 0 1 0 33.99.05l.16-.4c.47-1.08.5-2.13.17-3.04-.32-.9-.95-1.6-1.68-2.06-1.41-.89-3.54-1.06-4.9.36l-.17.2A22.87 22.87 0 0 0 25 6.01V3Zm-1 4c-3.86 0-7.49 1-10.64 2.74l-.36.2a22 22 0 1 0 22 0l-.36-.2A21.9 21.9 0 0 0 24 7ZM12.5 9.08a23.08 23.08 0 0 0-4.76 3.66 2.98 2.98 0 0 1-.44-.98c-.55-2.31 2.31-4.31 4.35-3.34.3.15.6.37.85.66Zm23 0a23.08 23.08 0 0 1 4.76 3.66c.17-.4.26-.77.3-1.12.2-2.33-2.32-3.74-4.1-3.14-.36.12-.69.32-.96.6ZM24 31a2 2 0 0 0 .86-3.8l-.91-.2a2 2 0 0 0 .05 4Zm-.64-4.93-1.34-4.94-.04-.14.05-.15 1.5-4.5.47-1.42.47 1.42 1.5 4.5.05.15-.04.14-1.34 4.94.37.1 7.55-13.42.88.5-7.55 13.42a3 3 0 1 1-2.53-.6ZM23.02 21 24 24.6l.98-3.59-.98-2.93-.98 2.93Z" clip-rule="evenodd"/></svg>
          <h3 class="subheader">Дата и время</h3>
          <p class="paragraph">24 мая 2024 г.<br>Начинаем в 16:00</p>
        </li>
      </ul>
    </div>
  </section>
</template>

<script setup></script>

<style lang="scss" scoped>
section {
  background-color: #C2CDCA;
  padding-bottom: 20px;
}

.heading {
  width: 107px;
}

.wrapper img {
  display: none;
}

ul {
  list-style: none;
  display: flex;
  flex-direction: column;
  row-gap: 25px;
  margin: 0;
  padding: 0;
}

li {
  display: grid;
  grid-template-columns: min-content auto;
}

svg {
  grid-column: 1 / -1;
  grid-row: 1 / 2;
  justify-self: center;
}

.subheader {
  grid-column: 1 / -1;
  grid-row: 2 / 3;
  color: #2A2A2A;
}

.paragraph {
  grid-column: 1 / -1;
  grid-row: 3 / 4;
  color: #2A2A2A;
}

@media(min-width: 768px) {
  section {
    padding-bottom: 60px;
  }

  .heading {
    width: 216px;
  }

  .wrapper {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 50px;
  }

  .wrapper img {
    display: block;
    width: 100%;
    max-width: 100%;
  }

  ul {
    align-self: center;
  }

  li {
    column-gap: 13px;
  }

  svg {
    grid-column: 1 / 2;
  }

  .subheader {
    grid-column: 2 / 3;
    grid-row: 1 / 2;
    text-align: left;
  }
  .paragraph {
    text-align: left;
  }
}
</style>