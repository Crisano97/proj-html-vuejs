<template>
  <div class="footer-top">
      <div class="footer-container left-container">
            <img src="../../assets/images/medical_logo_1x_dark.png" alt="">
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Placeat, molestias! Cupiditate ut iusto nisi dolore soluta voluptatibus hic, explicabo ipsum reiciendis pariatur minima. Velit, atque fuga. Officiis impedit quae ad!</p>
            <hr>
            <span>learn more about us</span>
            <div class="socials-container">
                <i class="fa-brands fa-square-facebook"></i>
                <i class="fa-brands fa-square-twitter"></i>
                <i class="fa-brands fa-youtube"></i>
                <i class="fa-brands fa-square-instagram"></i>
            </div>
      </div>
      <div class="footer-container middle-container">
            <h4>contact information</h4>
            <hr>
            <span>
                <i class="fa-solid fa-location-dot"></i>
                121 King Street, London United Kingdom
            </span>
            <span>
                <i class="fa-solid fa-phone-flip"></i>
                1.800.458.566
            </span>
        </div>
        <div class="footer-container right-container">
            <h4>medical departments</h4>
            <hr>
            <ul>
                <li v-for="(link, index) in footerLinksList" :key="index">
                    <i class="fa-solid fa-angle-right"></i>
                    <a :href="link.url" @click.prevent="">
                        {{ link.text }}
                    </a>
                </li>
            </ul>
            <button> view our departments</button>
      </div>
    </div>
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

    @import "../../styles/general.scss"; 

    div.footer-top{
    display: flex;

    div.footer-container{
        width: calc(100% / 3);
        padding-top: 4rem;
        padding-bottom: 4rem;
        color: $secondaryTextColor;
        font-weight: 100;
    }

    .left-container{
        padding-left: 3rem;
        img{
            width: 15rem;
        }

        p{
            line-height: 2rem;
            font-size: .8rem;
        }

        hr{
            margin-top: 2rem;
            margin-bottom: .5rem;
            color: $primaryTextColor;
        }

        span{
            text-transform: uppercase; 
        }
        .socials-container{
            display: flex;
            justify-content: flex-start;
            margin-top: 2rem;
            .fa-brands{
                font-size: 2rem;
                margin-right: .5rem;   
            }
            .fa-square-facebook{
                color: #3C5998;
            }
            .fa-youtube{
                color: #CD2322;
            }
            .fa-square-twitter{
                color: #5DB0EE;
            }
            .fa-square-instagram{
                color: #3C7099;
            }
        }
    }

    .middle-container{
        line-height: 2rem;
        padding-left: 2rem;
        h4{
            text-transform: uppercase;
        }
        hr{
            width: 2rem;
            margin: 1rem 0;
            color: $primaryTextColor;
        }
        span{
            display: block;
            font-size: .8rem;
        }
        i{
            color: $primaryTextColor;
            padding-right: .5rem;
        }
    }

    .right-container{
        h4{
            text-transform: uppercase;
        }
        hr{
            width: 2rem;
            margin: 1rem 0;
            color: $primaryTextColor;
        }
        ul{
            list-style: none;

            li{
            margin-bottom: 1rem;

            i{
                background-color: $primaryTextColor;
                padding: .3rem .5rem;
                border-radius: 50%;
                color: white;
                font-size: .8rem;
            }

            a{
                text-decoration: none;
                color: $secondaryTextColor;
                font-size: .8rem;
                padding-left: .5rem;
            }
            }
      }

      button{
        border: 2px solid $secondaryTextColor;
        background-color: transparent;
        padding: 1rem 4rem;
        text-transform: uppercase;
        color: $secondaryTextColor;
        cursor: pointer;
        margin-top: 2rem;
      }
    }
  }
</style>