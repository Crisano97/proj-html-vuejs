<template>
  <footer>
    <div class="footer-top">
      <div class="footer-container left-container">
        <img src="../assets/images/medical_logo_1x_dark.png" alt="">
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Placeat, molestias! Cupiditate ut iusto nisi dolore soluta voluptatibus hic, explicabo ipsum reiciendis pariatur minima. Velit, atque fuga. Officiis impedit quae ad!</p>
        <hr>
        <span>learn more about us</span>
      </div>
      <div class="footer-container middle-container">
        <h4>contact information</h4>
        <hr>
        <span>
          sdfsdf
        </span>
        <span>
          shdfhdhd
        </span>
      </div>
      <div class="footer-container right-container">
        <h4>medical departments</h4>
        <hr>
        <ul>
          <li v-for="(link, index) in footerLinksList" :key="index">
            <a :href="link.url">
              {{ link.text }}
            </a>
          </li>
        </ul>
        <button> view our departments</button>
      </div>
    </div>
    <div class="footer-bottom"></div>
  </footer>
</template>

<script>
export default {
  data:function(){
    return{
      footerLinksList: [
        {
          text:'Cardiology',
          url:'#',
        },
        {
          text:'Pediatrics',
          url:'#',
        },
        {
          text:'Disables Care',
          url:'#',
        },
        {
          text:'Pre-natal Care',
          url:'#',
        },
        {
          text:'Ultrasound Echocardiogram',
          url:'#',
        },
      ]
    }
  }
}
</script>

<style lang="scss">
  div.footer-top{
    display: flex;

    div.footer-container{
      width: calc(100% / 3);
      padding-top: 4rem;
      padding-bottom: 4rem;
    }

    .left-container{
      padding-left: 3rem;
      img{
        width: 15rem;
      }

      p{
        line-height: 2rem;

      }

      hr{
        margin-top: 1rem;
        margin-bottom: .5rem;
      }

      span{
        text-transform: uppercase;        
      }
    }

    .middle-container{
      line-height: 2rem;
      padding-left: 1rem;
      h4{
        text-transform: uppercase;
      }
      hr{
        width: 5rem;
        margin: 1rem 0;
      }
      span{
        display: block;
      }
    }

    .right-container{
      h4{
        text-transform: uppercase;
      }
      hr{
        width: 5rem;
        margin: 1rem 0;
      }
      ul{
        list-style: none;

        li{
          margin-bottom: 1rem;

          a{
            text-decoration: none;
            color: black;
          }
        }
      }

      button{
        // width: 20rem;
        border: 2px solid gray;
        background-color: transparent;
        padding: 1rem 4rem;
        text-transform: uppercase;
        color: gray;
      }
    }
  }

    div.footer-bottom{
      height: 10vh;
      background-color: red;
    }
</style>