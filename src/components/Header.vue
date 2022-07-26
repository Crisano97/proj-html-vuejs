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

    header{
        height: 80vh;
        width: 100%;
        background-image: url('../assets/images/header-image-homepage.jpg');
        background-size: cover;
        background-position: top;
        background-repeat: no-repeat;

        nav{
            width: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem;

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
                            color: blue;
                        }
                        &:last-child{
                            background-color: blue;
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
    }

</style>