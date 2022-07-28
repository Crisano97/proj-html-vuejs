<template>
  <section class="facilities">
        <div class="container">
            <SectionHead class="c-white" 
            :data="facilitiesSectionHead"
            />
            <img src="../../../assets/images/play-icon.png" alt="">
        </div>
  </section>
</template>

<script>

import SectionHead from '../SectionHead.vue';


export default {
    components:{
        SectionHead,
    },
    data:function(){
        return{
            facilitiesSectionHead: {
                imgUrl: '/images/icon-7.png',
                title: 'tour our facilities',
                text: 'Sed ut perspiciatis unde pmnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsia quae av ill inventore veritatis et quasi architecto beatae',
            },
        }
    }
}
</script>

<style lang="scss">
     section.facilities{
        height: 80vh;
        background-image: url('../../../assets/images/paralax-bg-tour-facilities.jpg');
        background-size: cover;
        background-position: center;       

        img{
            width: 3rem;
            margin-top: 2rem;
            cursor: pointer;
        }
    }
</style>