<template>
  <div class="info-container bg-color-1" v-if="item.id == 0">
        <h4>
            {{item.title}}
        </h4>
        <img :src="item.imgUrl" alt="divider">
        <p>
            {{item.text}}
        </p>
        <button>
            learn more
        </button>
  </div>
  <div class="info-container bg-color-2" v-else-if="item.id == 1">
        <h4>
            {{item.title}}
        </h4>
        <img :src="item.imgUrl" alt="divider">
        <p>
            {{item.text}}
        </p>
        <button>
            learn more
        </button>
  </div>
  <div class="info-container bg-color-3" v-else>
        <h4>
            {{item.title}}
        </h4>
        <img :src="item.imgUrl" alt="divider">
        <p>
            {{item.text}}
        </p>
        <button>
            learn more
        </button>
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

    @import "../../styles/general.scss";

    div.info-container{
        width: calc(100% / 3 );
        text-align: center;
        color: white;
        line-height: 2rem;
        padding: 3rem 1rem;

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
            cursor: pointer;
        }

        
    }

    .bg-color-1{
            background-color: $primaryColorLight;
    }
    .bg-color-2{
        background-color: $secondaryColorMid;
            
    }
   .bg-color-3{
        background-color: $primaryTextColor;
    }
</style>