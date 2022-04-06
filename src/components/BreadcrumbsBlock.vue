<template>
        <div class="breadcrumbs">
        <h2>Корзина</h2>
        <span>.............................</span>
        <h2>
          <a href="https://dimalmag.ru/wp-content/uploads/2021/04/texnical.png">Оформление заказа</a>
        </h2>
        <span>.............................</span>
        <h2>
          <a href="https://dimalmag.ru/wp-content/uploads/2021/04/texnical.png">Готово</a>
        </h2>
      </div>
</template>

<script>
export default {

}
</script>

<style style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto+Slab:wght@300;500&display=swap');

    .breadcrumbs {
      display: flex;
      justify-content: flex-start;
      align-items: center;
      h2 {
        margin: 0;
        font-family: 'Roboto Slab';
        font-style: normal;
        font-weight: 700;
        font-size: 30px;
        line-height: 44px;
        color: black
      }
      a {
        text-decoration: none;
        color: #CCCCCC;
        }
      span {
        padding: 0 20px 0 20px;
      }
    }
    @media(max-width: 479px) {
      .breadcrumbs {
        margin: 36px 0 0 16px;
        display: flex;
        flex-wrap: nowrap;
         overflow-x: auto;
         margin-bottom: 24px;

        h2 {
          font-family: 'Roboto Slab';
          font-style: normal;
          font-weight: 700;
          font-size: 20px;
          line-height: 28px;
          flex: 0 0 auto;
        }
      }
    }
</style>
