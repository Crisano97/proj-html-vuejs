<template>
  <header>
    <nav>
        <div class="logo-container">
            <img class="dark" src="../assets/images/medical_logo_1x_light.png" alt="">
        </div>
        <div class="menu-container">
            <ul class="menu">
                <li v-for="(link, index) in navLinks" :key="index">
                    <a :href="link.url">
                        {{ link.text }}
                    </a>
                </li>
            </ul>
        </div>
    </nav>
    <div class="container">
        <div class="element-container">
            <h1>Caring <span>For Life</span></h1>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis at sequi recusandae harum iusto. Commodi pariatur quae expedita repudiandae, animi aut inventore vero natus, cupiditate, ad cum vitae repellendus at.</p>
            <button>learn more</button>
        </div>
    </div>
  </header>
</template>

<script>
export default {
    data:function(){
        return{
            navLinks:[
                {
                    text: 'home',
                    url: '#'
                },
                {
                    text: 'about',
                    url: '#'
                },
                {
                    text: 'departments',
                    url: '#'
                },
                {
                    text: 'articles',
                    url: '#'
                },
                {
                    text: 'make appointments',
                    url: '#'
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

    @import "../styles/general.scss";

    header{
        height: 100vh;
        width: 100%;
        background-image: url('../assets/images/header-image-homepage.jpg');
        background-size: 100rem;
        background-position: top;
        background-repeat: no-repeat;

        nav{
            width: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 7rem;

            div.logo-container img{
                width: 10rem;
            }

            div.menu-container{
                // height: 3rem;
                width: 30rem;
                // background-color: red;

                ul.menu{
                    display: flex;
                    justify-content: space-between;
                    list-style: none;
                    align-items: center;

                    li{
                        &:first-child a{
                            color: $primaryTextColor;
                        }
                        &:last-child{
                            background-color: $primaryColorLight;
                            padding: .5rem 1rem;
                        }
                        a{
                            
                            text-decoration: none;
                            color: white;
                            text-transform: uppercase;
                            font-size: .7rem;

                        }
                    }
                }
            }
        }
        
        div.container{
            width: 52%;
            margin: 0 auto;
            padding-top: 9%;
            
            div.element-container{
                width: 31rem;
                display: flex;
                flex-direction: column;
                justify-content: space-around;
                align-items: flex-start;
                height: 12rem;
                color: white;
            }
            

            h1{
                font-weight: 100;
                font-size: 3rem;
                span{
                    color: $primaryTextColor;
                }
            }
            
            p{
                font-weight: 100;
                font-size:.8rem;
                line-height: 1.5rem;
            }

            button{
                background-color: $primaryColorLight;
                border: 0;
                padding:  .5rem 1rem;
                color: white;
                text-transform: uppercase;

            }
        }
    }

</style>