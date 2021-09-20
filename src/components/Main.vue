<template>
  <main>
      <div class="main-top">
        <div class="text-main-top">
            <p> -- Content goes here -- </p>

        </div>
      </div>
    <div class="main-bottom">
        <ul>
            <li><img src="../assets/img/buy-comics-digital-comics.png" alt=""><span>DIGITAL COMICS</span></li>
            <li><img src="../assets/img/buy-comics-merchandise.png" alt=""><span>DC MERCHANDISE</span></li>
            <li><img src="../assets/img/buy-comics-subscriptions.png" alt=""><span>SUBSCRIPTION</span></li>
            <li><img src="../assets/img/buy-comics-shop-locator.png" alt=""><span>COMIC SHOP LOCATOR</span></li>
            <li><img src="../assets/img/buy-dc-power-visa.svg" alt=""><span>DC POWER VISA</span></li>
        </ul>
    </div>
  </main>
</template>

<script>
export default {
  name: 'Main',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.main-top {
    display: flex;
    align-items: center;
    width: 100%;
    height: 150px;
    background-color: black;
    color: white;

    .text-main-top {
        margin: 0 auto;
        width: 70%;
        font-size: 25px;
    }
}

.main-bottom {
    display: flex;
    align-items: center;
    justify-content: space-around;
    width: 100%;
    height: 150px;
    background-color: #0282f9;

    ul {
        display: flex;
        align-items: center;
        justify-content: space-around;
        list-style: none;
        width: 70%;
        margin: 0 auto;

        li {
            display: flex;
            align-items: center;
            width: 16%;
            color: white;

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