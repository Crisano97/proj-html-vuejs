<template>
    <div class="section-type-container" v-if="doctorSectionHead">
        <img :src="doctorSectionHead.imgUrl" alt="">
        <h2>{{doctorSectionHead.title}}</h2>
        <hr>
        <span>
            {{doctorSectionHead.text}}
        </span>
    </div>
    <div class="section-type-container" v-else-if="servicesSectionHead">
        <img :src="servicesSectionHead.imgUrl" alt="">
        <h2>{{servicesSectionHead.title}}</h2>
        <hr>
        <span>
            {{servicesSectionHead.text}}
        </span>
    </div>
    <div class="section-type-container c-white" v-else-if="facilitiesSectionHead">
        <img :src="facilitiesSectionHead.imgUrl" alt="">
        <h2>{{facilitiesSectionHead.title}}</h2>
        <hr>
        <span>
            {{facilitiesSectionHead.text}}
        </span>
    </div>
    <div class="section-type-container c-white" v-else>
        <h2>{{appointmentSectionHead.title}}</h2>
        <hr>
        <span>
            {{appointmentSectionHead.text}}
        </span>
    </div>
</template>

<script>
export default {
    props:{
        'doctorSectionHead':{
            type: Object,
        },
        'servicesSectionHead':{
            type: Object,
        },
        'facilitiesSectionHead':{
            type: Object,
        },
        'appointmentSectionHead':{
            type:Object,
        }
    }
}
</script>

<style lang="scss">
    div.section-type-container{
        width: 70%;
        margin: 0 auto;

        h2{
            font-size: 2rem;
            text-transform: uppercase;
            font-weight: 100;
        }

        hr{
            width: 40%;
            margin: 2rem auto;
        }
    }

    .c-white{
        color:white;
    }
</style>