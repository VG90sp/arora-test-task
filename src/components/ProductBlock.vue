<template>
  <div class="product__order">
    <div class="product__order__novel" v-if="novel">
      <svg width="99" height="64" viewBox="0 0 99 64" fill="none" xmlns="http://www.w3.org/2000/svg">
<g filter="url(#filter0_dd_1293_428)">
<path d="M16 26C16 17.1634 23.1634 10 32 10H67C75.8366 10 83 17.1634 83 26V26C83 34.8366 75.8366 42 67 42H32C23.1634 42 16 34.8366 16 26V26Z" fill="#E30029"/>
<path d="M32.5947 31V29.9473L33.6816 29.7422V22.3115L32.5947 22.1064V21.0469H33.6816H35.4248L39.9912 28.3135L40.0322 28.2998V22.3115L38.7744 22.1064V21.0469H41.584H42.6709V22.1064L41.584 22.3115V31H39.9502L35.2744 23.7607L35.2334 23.7676V29.7422L36.4912 29.9473V31H32.5947ZM43.5254 31V29.9473L44.6123 29.7422V22.3115L43.5254 22.1064V21.0469H51.1064V23.6104H49.7666L49.6504 22.373H46.335V25.1895H49.8281V26.5225H46.335V29.6875H49.835L49.9512 28.4229H51.2773V31H43.5254ZM55.6182 31L53.3008 22.209L52.3574 22.1064V21.0469H56.0352V22.1064L54.9756 22.2637L56.1992 27.377L56.4521 28.4229L56.4932 28.4297L56.8076 27.377L58.79 21.0469H60.1367L62.1738 27.4795L62.4746 28.498H62.5156L62.7822 27.4795L64.0264 22.2637L62.9053 22.1064V21.0469H66.5146V22.1064L65.6328 22.209L63.3428 31H61.7568L59.7539 24.7314L59.501 23.8291H59.46L59.1934 24.7451L57.1768 31H55.6182Z" fill="white"/>
</g>
<defs>
<filter id="filter0_dd_1293_428" x="0" y="0" width="99" height="64" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">
<feFlood flood-opacity="0" result="BackgroundImageFix"/>
<feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha"/>
<feOffset dy="6"/>
<feGaussianBlur stdDeviation="8"/>
<feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.32 0"/>
<feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_1293_428"/>
<feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha"/>
<feOffset dy="1"/>
<feGaussianBlur stdDeviation="3"/>
<feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.24 0"/>
<feBlend mode="normal" in2="effect1_dropShadow_1293_428" result="effect2_dropShadow_1293_428"/>
<feBlend mode="normal" in="SourceGraphic" in2="effect2_dropShadow_1293_428" result="shape"/>
</filter>
</defs>
</svg>
    </div>
    <img :src="image">
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
    },
    novel: {
      type: String,
      required: false
    },
    image: {
      type: String,
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
    position: relative;
    margin-top: 40px;
    width: 60%;
    height: 215px;
    background: #F1F1F1;
    border-radius: 8px;

     &__novel {
        content: "";
        position: absolute;
        margin: 0;
        padding: 0;
     }

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
