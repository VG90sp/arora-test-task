<template>
<div class="sidebar">
    <h2>+358 баллов</h2>
    <p>Баллы начисляются в течении двух дней и доступны для использования при заказе от 500 руб. Только для зарегистрированных пользователей.</p>
    <p>Зарегистрируйтесь или войдите.</p>
    <h2 class="promo">Промокод</h2>
    <form action="URL">
      <input type="text" placeholder="введите промокод">
      <button class="sidebar__input_btn">Применить</button>
    </form>
    <div class="total">
    <div class="total__price">
      <span>Сумма заказа:</span>
      <span class="total__price__sale">4200</span>
      <span>3580</span>
    </div>
    <button class="btn_desktop">Далее</button>
    <button class="btn_mobile">Оформить заказ</button>
</div>
</div>
</template>

<script>

export default {
}
</script>

<style style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto+Slab:wght@300;500&display=swap');
  .sidebar {
      display: flex;
      flex-direction: column;
      box-shadow: 0px 1px 1px rgba(0, 0, 0, 0.25), 0px 0px 4px rgba(0, 0, 0, 0.16), 0px 4px 6px rgba(0, 0, 0, 0.16);
      border-radius: 8px;
      padding: 0 40px 40px 40px;

      h2 {
          margin: 40px 0 0 0;
          font-family: 'Roboto Slab';
          font-style: normal;
          font-weight: 700;
          font-size: 22px;
          line-height: 32px;
          color: #333333;
      }

      p {
          margin: 13px 0 0 0;
          font-family: 'Roboto Slab';
          font-style: normal;
          font-weight: 400;
          font-size: 14px;
          line-height: 20px;
          color: #333333;
      }

      input {
          border: 2px solid #808080;
          box-sizing: border-box;
          border-radius: 30px;
          width: 100%;
          height: 40px;
          padding-left: 16px;
          margin: 16px 0 16px 0;
          font-family: 'Roboto Slab';
          font-style: normal;
          font-weight: 400;
          font-size: 16px;
          line-height: 24px;
          color: #CCCCCC;
      }

      &__input_btn {
          display: flex;
          margin-left: auto;
          justify-content: center;
          align-items: center;
          width: 160px;
          height: 40px;
          background: #FFFFFF;
          border: 2px solid #CC693E;
          border-radius: 32px;
          font-family: 'Roboto Slab';
          font-style: normal;
          font-weight: 400;
          font-size: 16px;
          line-height: 24px;
          color: #CC693E;
      }

      .total {
          margin-top:  40px;

          .total__price {
              margin-right: auto;
          }
      }

@media(min-width: 961px) {
      .btn_mobile {
          display: none;
      }
}
  }
  @media(max-width: 479px){
      .sidebar {
          box-shadow: none;
          padding: 0 16px;
          margin-bottom: 64px;

          h2 {
              margin: 32px 0 0 0;
              font-size: 18px;
              line-height: 24px;
              margin-left: auto;
          }
          .promo {
              margin-right: auto;
              margin-left: 0;
              font-size: 22px;
              line-height: 32px;
          }

          p {
              font-size: 12px;
              line-height: 16px;
          }

          &__input_btn {
            width: 140px;
            font-size: 14px;
            line-height: 20px;
          }

          .total{
              margin-top: 32px;

            .total__price {
                margin-left: auto;
                margin-right: 0;

                span {
                    font-size: 16px;
                    line-height: 24px;
                }
            }
          }

          .btn_desktop {
              display: none;
          }

          .btn_mobile {
              height: 48px;
              font-size: 14px;
              line-height: 20px;
          }
      }
  }
</style>
