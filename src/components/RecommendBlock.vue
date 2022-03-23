<template>
  <div class="product_recommend">
    <div class="product_recommend__novel" v-if="novel">
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
      <img src="../assets/images/image-rec-1.jpg">
      <div class="product_recommend__composition">
        <span class="product_recommend__composition__name">{{ product_name }}</span>
        <p>{{ product_text }}</p>
      </div>
      <div class="product_recommend__btn_from_sum">
          <button class="btn_from_sum" v-if="from_sum">
              <span>{{ price }}</span>
          </button>
          <button class="btn_sum" v-else>
            <span>{{ price }}</span>
          </button>
      </div>
  </div>
</template>

<script>
export default {
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
    from_sum: {
      type: Boolean,
      required: false
    },
    novel: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto+Slab:wght@300;500&display=swap');

  .product_recommend {
      display: flex;
      position: relative;
      flex-direction: column;
      margin-top: 40px;
      margin-right: 16px;
      width:298px;
      border-radius:8px 8px 0 0;
      background: #F1F1F1;

     &__novel {
        content: "";
        position: absolute;
        margin: 0;
        padding: 0;
      }

      img {
          border-radius:8px 8px 0 0;
          width:298px;
      }

      &__composition {
          display: flex;
          flex-direction: column;
          padding: 16px;

          span {
              font-family: 'Roboto Slab';
              font-style: normal;
              font-weight: 700;
              font-size: 18px;
              line-height: 24px;
          }

          p {
              margin: 16px 0 0 0;
              font-family: 'Roboto Slab';
              font-style: normal;
              font-weight: 400;
              font-size: 14px;
              line-height: 20px;
              color: #666666;
          }
      }

      &__btn_from_sum {
          display: flex;
          justify-content: flex-end;
          padding: 0 16px 16px 0;

          .btn_from_sum {
              width: 134px;
              height: 40px;
              background: #FFFFFF;
              border: 2px solid #CC693E;
              border-radius: 32px;

              span {
                  font-family: 'Roboto Slab';
                  font-style: normal;
                  font-weight: 700;
                  font-size: 18px;
                  line-height: 24px;
                  color: #CC693E
              }
          }
          .btn_sum {
              width: 134px;
              height: 40px;
              background: #CC693E;
              border-radius: 32px;
              border: 2px solid #CC693E;

              span {
                  font-family: 'Roboto Slab';
                  font-style: normal;
                  font-weight: 700;
                  font-size: 18px;
                  line-height: 24px;
                  color: #FFFFFF;
              }
          }
      }
  }
</style>
