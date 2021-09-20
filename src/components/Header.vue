<template>
  <header>
      <img src="../assets/img/dc-logo.png" alt="">

      <ul>
          <li v-for='(link, index) in links' :key="index">
              <!-- attenzione a scrivere il ternario. servono i doppi apici -->
            <a :class="(link.current) ? 'active' : null"  :href="link.url">
                {{link.text}}
            </a>
          </li>
          
      </ul>
  </header>
</template>

<script>
export default {
  name: 'Header',

  data() {
      return {
          links: [
              {
                  text: 'CHARACTERS',
                  url: '#',
                  current: false,
              },
              {
                  text: 'COMICS',
                  url: '#',
                  current: true,
              },
              {
                  text: 'MOVIE',
                  url: '#',
                  current: false,
              },
              {
                  text: 'TV',
                  url: '#',
                  current: false,
              },
              {
                  text: 'GAMES',
                  url: '#',
                  current: false,
              },
              {
                  text: 'COLLECTIBLES',
                  url: '#',
                  current: false,
              },
              {
                  text: 'VIDEOS',
                  url: '#',
                  current: false,
              },
              {
                  text: 'FANS',
                  url: '#',
                  current: false,
              },
              {
                  text: 'NEWS',
                  url: '#',
                  current: false,
              },
              {
                  text: 'SHOP',
                  url: '#',
                  current: false,
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



header {
    height: 120px;
    width: 70%;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between;

    img {
        max-width: 80px;
    }

    ul {
        list-style: none;
        display: flex;

        li a {
            color: black;
            text-decoration: none;
            display: flex;
            padding: 0 10px;
            font-weight: 600;
            font-size: 12px;

            &:hover,
            &.active {
                color: $primary;
            }
        }
    }
}
</style>
