<template>
  <div class="info-container">
    <h4>{{item.title}}</h4>
    <img :src="item.imgUrl" alt="divider">
    <p>{{item.text}}</p>

    <button>learn more</button>
  </div>
</template>

<script>
export default {
    props:{
        'item':{
            type: Object,
        }
    }
}
</script>

<style lang="scss">
    div.info-container{
        width: calc(100% / 3 - 1rem);
        text-align: center;
        color: white;
        line-height: 2rem;

        p{
            font-size: .8rem;
        }

        button{
            border: 2px solid white;
            background-color: transparent;
            color: white;
            text-transform: uppercase;
            padding: .6rem 2rem;
            margin-top: 2rem;
        }
    }
</style>