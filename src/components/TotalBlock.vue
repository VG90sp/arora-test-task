<template>
<div class="total">
    <div class="total__price">
      <span>Сумма заказа:</span>
      <span class="total__price__sale">{{sale_price}}</span>
      <span>{{total_price}}</span>
    </div>
    <button>Далее</button>
</div>
</template>

<script>
export default {
  props: {
    sale_price: {
      type: String,
      Number,
      required: true
    },
    total_price: {
      type: String,
      Number,
      required: true
    }
  }
}
</script>

<style style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto+Slab:wght@300;500&display=swap');

  .total {
      display: flex;
      flex-direction: column;

      &__price {
          display: flex;
          align-items: center;
          justify-content: flex-end;
          font-family: 'Roboto Slab';
          font-style: normal;
          font-weight: 700;
          font-size: 18px;
          line-height: 24px;
          color: #333333;

          &__sale {
              color: #666666;
              padding: 0 4px 0 4px;
              text-decoration: line-through;
          }
      }
      button {
        width:100%;
        height: 64px;
        background: #CC693E;
        border-radius: 32px;
        border: 2px solid #CC693E;
        font-family: 'Roboto Slab';
        font-style: normal;
        font-weight: 500;
        font-size: 18px;
        line-height: 24px;
        color: #FFFFFF;
        margin-top: 32px;
      }
  }

</style>
