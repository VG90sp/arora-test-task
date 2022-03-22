<template>
  <div class="product__order">
    <img src="..\assets\images\image-1.jpg">
    <div class="product__order__composition">
      <span class="product__order__composition__product">{{ product_name }}</span>
      <p>{{ product_text }}</p>
      <div class="product__order__composition__amount">
          <span class="product__order__composition__amount__price">{{ price }}</span>
        <button class="left_btn" @click="lowCounter">-</button>
        <span class="counter">{{ counter }}</span>
        <button class="right_btn" @click="riseCounter">+</button>
        <span class="product__order__composition__amount__price">{{ price *  counter }}</span>
      </div>
    </div>
    <div class="product__order__button-close">
      <button>
      <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path fill-rule="evenodd" clip-rule="evenodd" d="M12 3C16.9706 3 21 7.02944 21 12C21 16.9706 16.9706 21 12 21C7.02944 21 3 16.9706 3 12C3 7.02944 7.02944 3 12 3ZM12 0C18.6274 0 24 5.37258 24 12C24 18.6274 18.6274 24 12 24C5.37258 24 0 18.6274 0 12C0 5.37258 5.37258 0 12 0Z" fill="#999999"/>
        <path fill-rule="evenodd" clip-rule="evenodd" d="M9.31066 7.18934C8.72487 6.60355 7.77513 6.60355 7.18934 7.18934C6.60355 7.77513 6.60355 8.72487 7.18934 9.31066L9.87868 12L7.18934 14.6893C6.60355 15.2751 6.60355 16.2249 7.18934 16.8107C7.77513 17.3964 8.72487 17.3964 9.31066 16.8107L12 14.1213L14.6893 16.8107C15.2751 17.3964 16.2249 17.3964 16.8107 16.8107C17.3964 16.2249 17.3964 15.2751 16.8107 14.6893L14.1213 12L16.8107 9.31066C17.3964 8.72487 17.3964 7.77513 16.8107 7.18934C16.2249 6.60355 15.2751 6.60355 14.6893 7.18934L12 9.87868L9.31066 7.18934Z" fill="#999999"/>
      </svg>
      </button>
    </div>
  </div>
</template>

<script>
export default {

  data: function () {
    return {
      counter: 1
    }
  },

  props: {
    product_name: {
      type: String,
      Number,
      required: true
    },
    product_text: {
      type: String,
      Number,
      required: true
    },
    price: {
      type: String,
      Number,
      required: true
    }
  },

  methods: {
    riseCounter: function () {
      this.counter++
    },
    lowCounter: function () {
      this.counter--
    }
  }
}
</script>

<style style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto+Slab:wght@300;500&display=swap');

.product__order {
    display: flex;
    margin-top: 40px;
    width: 60%;
    height: 215px;
    background: #F1F1F1;
    border-radius: 8px;

    img {
          border-radius:8px 0 0 8px;
          width:185px;
          height:215px;
    }

    &__button-close {
        display: flex;
        height: 24px;
        padding: 20px 16px 0 0;

          button {
            padding: 0;
            width: 24px;
            border: 0;
            cursor: pointer;
      }
    }

    &__composition {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        padding-left: 40px;
        width: 100%;

        &__product {
          font-family: 'Roboto Slab';
          font-style: normal;
          font-weight: 700;
          font-size: 22px;
          line-height: 32px;
          color: #000000;
          padding-top: 16px;
        }

        p {
          font-family: 'Roboto Slab';
          font-style: normal;
          font-weight: 400;
          font-size: 14px;
          line-height: 20px;
          color: #666666;
          margin: 0;
          padding-top: 10px;
        }

     &__amount {
        display: flex;
        align-items: flex-center;
        margin-left: auto;
        padding-top: 24px;

        &__price {
            display: flex;
            padding: 0 16px 0 16px;
            align-items: center;
            font-family: 'Roboto Slab';
            font-style: normal;
            font-weight: 500;
            font-size: 18px;
            line-height: 24px;
        }

        .counter {
          font-family: 'Roboto Slab';
          font-style: normal;
          font-weight: 500;
          font-size: 18px;
          line-height: 24px;
          align-items: center;
          text-align: center;
          color: #666666;
          background:white;
          border-top: 2px solid #CC693E;
          border-bottom: 2px solid #CC693E;
          padding: 8px 16px;
        }
        .left_btn {
            border-radius: 30px 0px 0px 30px;
            border: 2px solid #CC693E;
            width: 40px;
            background: white;
        }
        .right_btn {
            border-radius: 0px 30px 30px 0px;
            border: 2px solid #CC693E;
            width: 40px;
            background: white;
        }
    }
    }
}

</style>
