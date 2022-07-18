<template>
  <footer>
    <!-- inseriamo il background e creiamo all' interno due div che conterrano le liste e il logo -->
    <div class="container">
        <!-- LISTE -->
        <div class="container-ul">
            <div>
                <ul>
                    <li> <h2>DC COMICS</h2> </li>
                    <li class="font" v-for="(element, index) in listComics" :key="index">
                    <a @click.prevent href="">  {{  element.listItem }} </a>
                    </li>
                </ul>
                <ul>
                    <li> <h2>SHOP</h2> </li>
                    <li class="font" v-for="(element, index) in listShop" :key="index">
                    <a @click.prevent href="">  {{  element.listItem }} </a>
                    </li>
                </ul>
            </div>
            <div class="flex-ul">
                <ul class="ul-special">
                    <li> <h2>DC</h2> </li>
                    <li class="font" v-for="(element, index) in listDC" :key="index">
                    <a @click.prevent href="">  {{  element.listItem }} </a>
                    </li>
                </ul>
                <ul>
                    <li> <h2>SITES</h2> </li>
                    <li class="font" v-for="(element, index) in listSite" :key="index">
                    <a @click.prevent href="">  {{  element.listItem }} </a>
                    </li>
                </ul>
            </div>
        </div>
        <!-- IMMAGINE -->
        <div>
            <img class="bg-logo" src="../assets/dc-logo-bg.png" alt="">
        </div>
    </div>
    <div class="index-definer">
        <section class="container2">
            <div class="signUpBorder">
                <a @click.prevent href=""> SIGN-UP NOW!</a>  
            </div>
            <div>
                <ul class="footerUL">
                    <li>
                        <h2>FOLLOW US</h2>
                    </li>
                    <li>
                        <img src="../assets/footer-facebook.png" alt="">
                    </li>
                    <li>
                        <img src="../assets/footer-periscope.png" alt="">
                    </li>
                    <li>
                        <img src="../assets/footer-pinterest.png" alt="">
                    </li>
                    <li>
                        <img src="../assets/footer-twitter.png" alt="">
                    </li>
                    <li>
                        <img src="../assets/footer-youtube.png" alt="">
                    </li>
                </ul>
            </div>
        </section>
        
    </div>
    <div class="bg-last"></div>
  </footer>
</template>

<script>
export default{
    data: function(){
        return{
            listComics:[
                {
                    listItem: 'Characters'
                },
                {
                    listItem: 'Comics'
                },
                {
                    listItem: 'Movies'
                },
                {
                    listItem: 'TV'
                },
                {
                    listItem: 'Games'
                },
                {
                    listItem: 'Videos'
                },
                {
                    listItem: 'News'
                }
            ],

            listShop:[
                {
                    listItem: 'Shop DC'
                },
                {
                    listItem: 'Shop DC collectibles'
                },
                
            ],

            listDC:[
                {
                    listItem: 'Terms of use'
                },
                {
                    listItem: 'Privacy Policy'
                },
                {
                    listItem: 'Ad choices'
                },
                {
                    listItem: 'Advertising'
                },
                
                {
                    listItem: 'Jobs'
                },
                {
                    listItem: 'Subscription'
                },
                {
                    listItem: 'Talent Workshop'
                },
                {
                    listItem: 'CPSC certificates'
                },
                {
                    listItem: 'Rating'
                },
                {
                    listItem: 'Shop help'
                },
                {
                    listItem: 'Contact us'
                }
            ],

            listSite:[
            {
                listItem: 'DC'
            },
            {
                listItem: 'MAD magazine'
            },
            {
                listItem: 'DC kids'
            },
            {
                listItem: 'DC universe'
            },
            {
                listItem: 'DC power visa'
            },
            ]
        }
    }
}

</script>


<style scoped lang="scss">
footer{
    background-image: url(../assets/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;
}
.container{
    display: flex;
    max-width: 1200px;
    margin: 0 auto;
    justify-content: space-between;
    height: 380px;
}
.container2{
    display: flex;
    max-width: 1200px;
    margin: 0 auto;
    justify-content: space-between;
    align-items: center;
}
.container-ul{
    
    color: white;
    display: flex;
}
ul li{
    list-style: none;
}
ul{
    padding: 30px;
}
.flex-ul{
    display: flex;
}
.font{
    font-size: 14px;
   
}
li h2{
    padding-bottom: 10px;
}
a{
    text-decoration: none;
    color: rgb(185, 184, 184);
}
.bg-logo{
    position: relative;
    bottom: 106px;
    z-index: 1;
}
.index-definer{
    background-color: rgb(51, 51, 51);
    position: relative;
    z-index: 50;
}
.signUpBorder{
    padding: 12px;
    border: solid 3px rgb(80, 80, 231);
    font-weight: bolder;
    height: 50px;
}
.footerUL{
    display: flex;
}
.footerUL li{
    padding: 10px
}
.footerUL li h2{
    color: rgb(80, 80, 231);;
}
.bg-last{
    background-color: rgb(22, 22, 22);
    height: 130px
}

</style>