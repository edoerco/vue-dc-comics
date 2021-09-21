<template>
  <footer>
    <div class="footer-top">
      <div class="container-top">
        <div class="col-left-top">
          <h3>DC COMICS</h3>
          <ul>
            <li>Characters</li>
            <li>Comics</li>
            <li>Movies</li>
            <li>TV</li>
            <li>Games</li>
            <li>Videos</li>
            <li>News</li>
          </ul>

          <h3>SHOP</h3>
          <ul>
            <li>Shop DC</li>
            <li>Shop Dc Collectibles</li>
          </ul>

          <h3>DC</h3>
          <ul>
            <li>Terms Of Use</li>
            <li>Privacy policy (New)</li>
            <li>AD Choices</li>
            <li>Advertising</li>
            <li>Jobs</li>
            <li>Subscriprions</li>
            <li>Talent Workshops</li>
            <li>CPsc Certificates</li>
            <li>Ratings</li>
            <li>Shop Help</li>
            <li>Contact Us</li>
          </ul>

          <h3>SITES</h3>
          <ul>
            <li>DC</li>
            <li>MAD Magazine</li>
            <li>DC Kids</li>
            <li>DC Universe</li>
            <li>DC Power visa</li>
          </ul>
        </div>
        <div class="col-right-top">
          <img src="../assets/img/dc-logo-bg.png" alt="dc big logo">
        </div>
      </div>
    </div>
    <div class="footer-bottom">
      <div class="container-bottom">
        <div class="col-left-bottom">
          <button>SIGN-UP NOW!</button>
        </div>

        <div class="col-right-bottom">
          <h3>FOLLOW US</h3>
          <img src="../assets/img/footer-facebook.png" alt="">
          <img src="../assets/img/footer-twitter.png" alt="">
          <img src="../assets/img/footer-youtube.png" alt="">
          <img src="../assets/img/footer-pinterest.png" alt="">
          <img src="../assets/img/footer-periscope.png" alt="">
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import "../style/vars";


.footer-top {
  height: 400px;
  width: 100%;
  background-image: url(../assets/img/footer-bg.jpg);
  background-size: cover;
  background-position: top;

  .container-top{
    display: flex;
    justify-content: space-between;
    width: 70%;
    height: 100%;
    margin: 0 auto;

    .col-left-top {
      display: flex;
      flex-direction: column;
      flex-wrap: wrap;
      width: 40%;
      height: 100%;
      padding: 30px 0;

      h3 {
        color: $light;
        margin: 20px 0; 
      }

      li {
        font-size: 14px;
        color: grey;
        width: 150px;
        margin: 5px 0;
      }
    }

    .col-right-top {
      width: 600px;

      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
    }
  }
}

.footer-bottom {
  height: 120px;
  width: 100%;
  background-color: #303030;

  .container-bottom {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 100%;
    width: 70%;
    margin: 0 auto;

    .col-left-bottom button {
      width: 150px;
      height: 50px;
      background-color: #303030;
      border: 2px solid $primary;
      color: white;
      font-size: 17px;

      &:hover {
        cursor: pointer;
      }
    }

    .col-right-bottom {
      display: flex;
      align-items: center;

      img {
        margin: 0 10px;

        &:hover {
          cursor: pointer;
        }
      }

       h3 {
        margin-right: 20px;
        color: $primary;

        &:hover {
          cursor: pointer;
        }
      }
    }
  }
}
</style>