<template>
  <main>
    <AnimateCircle class="st-orange" />
    <div class="container">
      <h2>Связаться со мной:</h2>
      <ul>
        <li><span>Телефон:</span> <a href="tel:+7 996 634 86 90">+7 996 634 86 90</a></li>
        <li><span>E-mail:</span> <a href="mailto:natalykliimi@gmail.com">natalykliimi@gmail.com</a></li>
        <li><span>Telegram:</span> <a href="https://t.me/Kliimi">@Kliimi</a></li>
        <li><span>Github:</span> <a href="https://github.com/Kliimi">@Kliimi</a></li>
      </ul>
    </div>
  </main>
</template>

<script>
export default {
  name: 'ContactsPage',
  head: {
    title: 'Связаться со мной'
  }
}
</script>

<style lang="scss" scoped>
main {
  flex-direction: column;
  align-items: center;
  @include sm {
    padding-top: 30%;
  }
}
.container {
  position: relative;
  top: 100px;
  & > ul {
    flex-direction: column;
    gap: 1em;
    font-size: 1.2em;
    li > span {
      font-weight: bolder;
    }
  }
  @include sm {
    top: 50px;
    ul {
      text-align: center;
    }
  }
}

</style>
