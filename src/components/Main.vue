<template>
    <main>
        <div class="main-top">
            <div class="icon-main-top">
                <div class="current-series">
                    <h3>CURRENT SERIES</h3>
                </div>
                <div class="icon" v-for="(card, index) in cards" :key="index">
                    <div class="img-box">
                        <img :src="card.thumb" :alt="card.series"> 
                    </div>
                    <span>{{card.series.toUpperCase()}}</span>
                </div>
            </div>
            <button>LOAD MORE</button>
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
import cards from '@/data/dc-comics.js'


export default {
  name: 'Main',
//   devo importare 'array'

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
            ],
            cards: cards
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
    flex-direction: column;
    width: 100%;
    background-color: $dark;
    color: $light;

    .current-series{
        position: absolute;
        top: -25px; 
        left: 30px;
        background-color: $primary;
        padding: 10px 30px;
    }

    .icon-main-top {
        position: relative;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
        align-items: baseline;
        margin: 0 auto;
        width: 70%;
        height: 100%;
        font-size: 25px;
        padding: 30px;

        .icon {
            display: flex;
            flex-direction: column;
            justify-content: center;
            margin: 10px 0;
            width: calc(100% / 6);

            .img-box {
                padding: 15px;
                width: 100%;
                height: 210px;

                img {
                    object-fit: cover;
                    object-position: top;
                    height: 100%;
                    width: 100%;
                }
            }

            span {
                padding: 15px;
                font-size: 14px;
            }

        }
    }

    button {
        color: $light;
        background-color: $primary;
        width: 200px;
        height: 40px;
        border-style: none;
        margin-bottom: 20px;
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
            justify-content: center;
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