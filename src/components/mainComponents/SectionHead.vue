<template>
    <div class="section-type-container">
        <img :src="data.imgUrl" alt="">
        <h2 :class="{'text-uppercase' : data.imgUrl}">{{data.title}}</h2>
        <hr>
        <span>
            {{data.text}}
        </span>
    </div>
    
</template>

<script>
export default {
    props:{
        'data':{
            type: Object,
        },
        
    }
}
</script>

<style lang="scss">
    div.section-type-container{
        width: 70%;
        margin: 0 auto;

        h2{
            font-size: 2rem;
            font-weight: 400;
        }

        hr{
            width: 40%;
            margin: 2rem auto;
        }

        span{
            font-weight: 400;
        }

        .text-uppercase{
            text-transform: uppercase;
        }
    }

</style>