<template>
  <footer>
    <div class="footer-top">
      <div class="footer-container">
        <img src="../assets/images/medical_logo_1x_dark.png" alt="">
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Placeat, molestias! Cupiditate ut iusto nisi dolore soluta voluptatibus hic, explicabo ipsum reiciendis pariatur minima. Velit, atque fuga. Officiis impedit quae ad!</p>
        <hr>
        <span>learn more about us</span>
      </div>
      <div class="footer-container">
        <h3>contact information</h3>
        <hr>
        <span>
          sdfsdf
        </span>
        <span>
          shdfhdhd
        </span>
      </div>
      <div class="footer-container">
        <h3>medical departments</h3>
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
    height: 60vh;
    background-color: green;
    display: flex;

    div.footer-container{
      width: calc(100% / 3);
      height: 100%;
      background-color: red;
      border: 2px solid white;
      padding: 1rem;
    }
  }

    div.footer-bottom{
      height: 10vh;
      background-color: bisque;
    }
</style>