<template>
    <div id="sidemenu">
    <button class="sidemenu__btn" v-on:click="navOpen=!navOpen" v-bind:class="{active:navOpen}">
        <span class="top"></span>
        <span class="mid"></span>
        <span class="bottom"></span>
    </button>
    <transition name="translateX">
      <nav v-show="navOpen">
        <div class="sidemenu__wrapper">
          <ul class="sidemenu__list">
            <li class="sidemenu__item"><a href="">Меню</a></li>
            <li class="sidemenu__item"><a href="">О нас</a></li>
            <li class="sidemenu__item"><a href="">Корзина</a></li>
          </ul>
        </div>
      </nav>
    </transition>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      navOpen: false
    }
  }
}
</script>

<style style lang="scss">
#sidemenu {
    width: 40px;
  nav {
    background: white;
    position: fixed;
    top: 0;
    right: 40%;
    z-index: 99;
  }

  .sidemenu {
    &__btn {
      display: block;
      height: 40px;
      background: white;
      border: none;
      position: relative;
      z-index: 100;
      appearance: none;
      cursor: pointer;
      outline: none;

      span {
        display: block;
        width: 35px;
        height: 5px;
        margin: auto;
        background: black;
        position: absolute;
        top: 0;
        bottom: 0;
        left: 0;
        right: 0;
        border-radius: 13px;
        transition: all .4s ease;

        &.top {
          transform: translateY(-8px);
        }

        &.bottom {
          transform: translateY(8px);
        }
      }
      &.active{
        .top {
          transform: rotate(-45deg);
        }
        .mid{
          transform: translateX(-20px) rotate(360deg);
          opacity: 0;
        }
        .bottom {
          transform: rotate(45deg);
        }
      }

    }

    &__wrapper {
      padding-top: 5px;
    }

    &__list {
      padding-top: 5px;
      list-style:none;
      padding: 0;
      margin: 0;
    }

    &__item {
      a {
        text-decoration: none;
        line-height: 16px;
        font-size: 12px;
        padding: 2px;
        display: block;
        color: black;
        transition: .4s ease;
      }
    }
  }
}
</style>
