<template>
    <div class="element-container" v-if="feature">
        <img :src="feature.imgUrl" alt="">
        <h3>
            {{ feature.title }}
        </h3>
        <p>
            {{ feature.text }}
        </p>
    </div>
    <div class="service-element" v-else-if="service">
            <img :src="service.imgUrl" alt="">
            <h3>
                {{ service.title }}
            </h3>
            <p>
                {{ service.text }}
            </p>
    </div>
</template>

<script>
export default {
    props:{
        'feature' : {
            type: Object,
        },
        'service':{
            type: Object,
        }
    }
}
</script>

<style lang="scss">
    div.element-container{
        width: calc(100% / 4 - .1rem);
        font-size: .7rem;

        h3{
            text-transform: uppercase;
            font-weight: 500;
        }

        img{
            width: 3rem;
        }
    }

    div.service-element{
        width: 30%;
        font-size: .7rem;
        margin-bottom: 4rem;

        h3{
            text-transform: uppercase;
            font-weight: 400;
        }
        
        p{
            font-weight: 300;
        }

        img{
            width: 3rem;
        }
    }
</style>