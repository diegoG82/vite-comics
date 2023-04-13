<script>
export default {
  name: "appFooter",
};
</script>

<template>
  <div class="footer">
    <div class="topfooter-container">
      <div class="top-footer flex">
        <div class="footer-list flex">
          <div class="dclist flex">
            <div class="card">
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
              <ul>
                <h3>SHOP</h3>
                <li>Shop DC</li>
                <li>Shop DC Collectibles</li>
              </ul>
            </div>
            <div class="card">
              <ul>
                <h3>DC</h3>
                <li>Terms of Use</li>
                <li>Privacy policy(New)</li>
                <li>Ad Choices</li>
                <li>Advertising</li>
                <li>Jobs</li>
                <li>Subscriptions</li>
                <li>Talent Workshops</li>
                <li>CPSC Certificates</li>
                <li>Ratings</li>
                <li>Shop Help</li>
                <li>Contact Us</li>
              </ul>
            </div>
            <div class="card">
              <ul>
                <h3>SITES</h3>
                <li>DC</li>
                <li>MAD Magazine</li>
                <li>DC Kids</li>
                <li>DC Universe</li>
                <li>DC Power Visa</li>
              </ul>
            </div>
          </div>
        </div>
        <div class="footer-logo flex">
          <img class="biglogo" src="../img/dc-logo-bg.png" alt="" />
        </div>
      </div>
    </div>
    <div class="bottomfooter-container flex">
       <div class="bottom-footer flex">
       <div class="bottom-button flex"><button>SIGN-UP NOW!  </button></div>
       <div class="bottom-social flex">
        <ul class="flex">
            <li><p>FOLLOW US</p></li>
            <li><img src="../img/footer-facebook.png" alt=""></li>
            <li><img src="../img/footer-twitter.png" alt=""></li>
            <li><img src="../img/footer-youtube.png" alt=""></li>
            <li><img src="../img/footer-pinterest.png" alt=""></li>
            <li><img src="../img/footer-periscope.png" alt=""></li>
        </ul>
       </div>
       </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.topfooter-container {
  width: 80%;
  height: 550px;
  margin: 0 auto;
}

.footer-list {
  width: 50%;
  margin-top: 80px;

  .dclist {
    width: 70%;
    height: 400px;
    // border: 1px solid white;
    flex-wrap: wrap;
  }

  .card {
    width: calc(100% / 3);
  }

  h3 {
    color: white;
    padding: 15px 0;
  }

  li {
    list-style: none;
    color: gray;
    padding: 2px 0;
  }
}

.footer-logo {
  width: 50%;
  justify-content: center;
  position: relative;
}

.biglogo {
  right: 120px;
  position: absolute;
  transform: scale(1.2);
}

.footer {
  position: relative;
  background: url(../img/footer-bg.jpg);
  background-size: cover;
}

.bottomfooter-container  {
  position: relative;
  height: 80px;
  z-index: 100;
  background-color: rgb(48, 48, 48);
  .bottom-footer{
    width:80%;
    height: 100%;
    margin: 0 auto;
    .bottom-button{
        width: 50%;
        height: 100%;
        flex-wrap: nowrap;
        align-items: center;
        button{
            padding:10px;
            border: 5px solid rgb(2, 130, 249);
            background: none;
            color: white;
            justify-content: center;
        }
        
    }
    .bottom-social{
        width: 50%;
        height: 100%;
        flex-wrap: nowrap;
        align-items: center;
        justify-content: end;
        ul{
            gap: 10px;
            align-items: center;
        }
        li{
            list-style: none;
        }
        p{
            color: rgb(2, 130, 249);
        }
    }

  }
}
</style>
