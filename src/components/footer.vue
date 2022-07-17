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
    height: 380px;
    background-image: url(../assets/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;
}
.container{
    display: flex;
    max-width: 1200px;
    margin: 0 auto;
    justify-content: space-between;
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
</style>