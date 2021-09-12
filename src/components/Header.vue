<template>
    <div class = "header-full">
        <div class = "logo-container">
          <img src = "../assets/molisana-logo.png" alt="">
        </div>
        <nav>
            <ul>
                <!-- la :key serve a vuejs per identificare l'elemento in maniera univoca. Quindi gli attribuiamo un valore univoco. -->

                <li v-for = "element in navList" :key = "element.id">
                    <a href="element.link">{{element.name}}</a>
                </li>
            </ul>
        </nav>
    </div>
</template>


<script>
        /*  'Home',
            'Prodotti',
            'Chi Siamo',
            'Contatti' */

    export default {
        name: 'Header',
        //il componente ascolta /recepisce la prop di nome nav
        props:[
            'navList',
            'nomeSaluto'
        ]
    }
</script>

<style lang="scss" scoped>
    
    .header-full {
        .logo-container{
            text-align:center;
            img {
                max-width: 100px;
            }
        }
        nav{
            ul{
                display: flex;
                list-style: none;
                justify-content: center;
                font-size: 14px;
                font-weight: bold;
                
                li{
                    height: 50px;
                    line-height: 50px;
                    padding: 0 10px;
                    cursor: pointer;
                    
                    &:hover {
                        background-color: #cee;
                    }
                }
            }
        }
    }


</style>