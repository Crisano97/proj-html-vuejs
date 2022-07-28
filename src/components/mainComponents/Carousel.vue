<template>
  <div class="carousel-container">
      <div class="container">
            <div class="carousel">
                <img :src="slide.imgUrl" alt="carousel image"
                v-for="(slide, slideIndex) in slides" :key="slideIndex"
                >
            </div>
      </div>
    </div>
</template>

<script>
export default {
    data:function(){
        return{
            slides:[
                {
                    imgUrl: '/images/client-logos-3.png'
                },
                {
                    imgUrl: '/images/client-logos-1.png'
                },
                {
                    imgUrl: '/images/client-logos-4.png'
                },
                {
                    imgUrl: '/images/client-logos-2.png'
                },
            ]
        }
    }
}
</script>

<style lang="scss">
     div.carousel-container{
        background-image: url('../../assets/images/rgb-gradient-bar-for-logo-carrasel.jpg');

        div.carousel{
            display: flex;
            justify-content: space-between;
            overflow: hidden;
            img{
                position: relative;
                animation: slide linear 10s infinite;
            }
            @keyframes slide {
                0%{right: 0}
                40%{right: 90rem;}
                53%{bottom: -12rem;}
                54%{right: -65rem;}
                55%{bottom: 0;}
                80%{right: 0;}
                100%{right: 0}
            }
        }
    }
</style>