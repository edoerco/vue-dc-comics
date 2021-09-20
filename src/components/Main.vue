<template>
  <main>
      <div class="main-top">
        <div class="text-main-top">
            <p> -- Content goes here -- </p>

        </div>
      </div>
    <div class="main-bottom">
        <ul>
            <li v-for="(icon, index) in icons" :key="index">
                <img :src="require(`../assets/img/${icon.url + icon.path + icon.extension}`)" :alt="icon.text"><span>{{icon.text}}</span>
            </li>
        </ul>
    </div>
  </main>
</template>

<script>
export default {
  name: 'Main',

  data() {
      return {
          icons: [
                {
                    url: 'buy-comics',
                    path: '-digital-comics',
                    extension: '.png',
                    text: 'DIGITAL COMICS'

                },
                {
                    url: 'buy-comics',
                    path: '-merchandise',
                    extension: '.png',
                    text: ' DCMERCHANDISE'
                },
                {
                    url: 'buy-comics',
                    path: '-subscriptions',
                    extension: '.png',
                    text: 'SUBSCRIPTIONS'
                },
                {
                    url: 'buy-comics',
                    path: '-shop-locator',
                    extension: '.png',
                    text: 'COMIC SHOP LOCATOR'
                },
                {
                    url: 'buy-dc',
                    path: '-power-visa',
                    extension: '.svg',
                    text: 'POWER VISA'
                }
            ]
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import "../style/vars";
  @import "../style/mixins";


.main-top {
    @include center(vertical);
    width: 100%;
    height: 150px;
    background-color: $dark;
    color: $light;

    .text-main-top {
        margin: 0 auto;
        width: 70%;
        font-size: 25px;
    }
}

.main-bottom {
    @include center(vertical);
    justify-content: space-around;
    width: 100%;
    height: 150px;
    background-color: $primary;

    ul {
        @include center(vertical);
        justify-content: space-around;
        list-style: none;
        width: 70%;
        margin: 0 auto;

        li {
            @include center(vertical);
            width: 16%;
            color: $light;

            span {
                font-size: 12px;
                margin-left: 10px;
            }
        }

    }

    img {
        max-width: 50px;
        max-height: 50px;
    }
}
</style>