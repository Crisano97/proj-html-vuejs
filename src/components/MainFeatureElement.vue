<template>
  <div class="feature-element-container">
    <img :src="feature.imgUrl" alt="">
    <h3>{{ feature.title }}</h3>
    <p>{{ feature.text }}</p>
  </div>
</template>

<script>
export default {
    props:{
        'feature' : {
            required: true,
            type: Object,
        }
    }
}
</script>

<style lang="scss">
    div.feature-element-container{
        width: calc(100% / 4 - .1rem);
        font-size: .7rem;

        h3{
            text-transform: uppercase;
        }

        img{
            width: 3rem;
        }
    }
</style>