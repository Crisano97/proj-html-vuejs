<template>
  <div class="card">
    <img :src="doctor.imgUrl" :alt="doctor.name">
    <div class="info">
        <h4>{{doctor.name}}</h4>
        <span>{{doctor.role}}</span>
        <p>{{doctor.description}}</p>
        <div class="socials-container">
            <i class="fa-brands fa-square-facebook"></i>
            <i class="fa-brands fa-square-twitter"></i>
            <i class="fa-brands fa-square-instagram"></i>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    props:{
        doctor:{
            required: true,
            type: Object,
        }
    }
}
</script>

<style lang="scss">
    div.card{
        width: calc(100% / 3 - 1rem);
        background-color: white;
        margin-top: 3rem;
        img{
            width: 100%;
        }

        div.info{
            padding: 1rem;
            text-align: left;
            
            h4{
                text-transform: uppercase;
                
            }

            p{
                margin: 2rem 0;
            }

            .socials-container{
                display: flex;
                justify-content: flex-start;

                .fa-brands{
                    font-size: 2rem;
                    margin-right: .5rem;   
                }
                .fa-square-facebook{
                    color: #3C5998;
                }
                .fa-square-twitter{
                    color: #5DB0EE;
                }
                .fa-square-instagram{
                    color: #3C7099;
                }
            }
        }
    }
</style>