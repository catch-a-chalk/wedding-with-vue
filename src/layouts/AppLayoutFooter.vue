<template>
  <footer>
    <div class="wrapper">
      <ul>
        <li>
          <a href="/">
            <img src="../assets/images/icons/icon-whatsapp.svg" alt="What's App"/>
          </a>
        </li>
        <li>
          <a href="/">
            <img src="../assets/images/icons/icon-telegram.svg" alt="Telegram"/>
          </a>
        </li>
        <li>
          <a href="/">
            <img src="../assets/images/icons/icon-heart.svg" alt="16cc"/>
          </a>
        </li>
      </ul>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
footer {
  background-color: #D3D3D3;
}

ul {
  width: 100%;
  list-style: none;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  margin: 0;
  padding: 15px 0;
}

li {
  &:last-child {
    grid-column: 4 / 5;
  }
}

a {
  padding: 15px;
}

img {
  width: 40px;
}

@media(min-width: 768px) {
  ul {
    grid-template-columns: repeat(10, 1fr);
  }

  li {
  &:last-child {
    grid-column: 10 / 11;
  }
}
}
</style>