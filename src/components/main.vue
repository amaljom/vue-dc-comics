<template>
  <main>
    
    <!-- QUA INSERIAMO L'IMMAGINE -->
    <div class="container black-band">  </div>
    <!-- CREO UN DIV PER CONTENERE TUTTI GLI ELEMENTI CHE DOVRO INSERIRE COME COMPONENT -->
    
    <section class="comics-container">
        <div class="posizionamento-elementi">
            <div class="button-current-series">
                <a @click.prevent href="#"> <p>CURRENT SERIES</p> </a>
            </div>
           <div class="wrapper-comics">
                <ComicsTemplate v-for="(item, index) in dinamicComicsList"
                    :key="index"
                    :img="item.thumb"
                    :series="item.series"
                    :price="item.price"
                    :type="item.type"  />
           </div>
           <div class="button-loader">
               <a @click.prevent href="#"><p>Load more</p></a> 
           </div>
        </div>
    </section>
    <!-- div azzurro cche richiamo con un secondo component -->
    <div class="content-azzurro ">
            <div class="posizionamento-elementi content-container content-container-images">
                <ul>
                    <BlueBandComponents v-for="(item, index) in listImagesForBlueBand"
                        :key="index"
                        :img="item.image"
                        :text="item.textImage"/>
                </ul>
            </div>
        </div>
  </main>
</template>

<script>
import ComicsTemplate from './ComicsTemplate'
import BlueBandComponents from "./BlueBandComponents.vue"
export default{

    components:{
        ComicsTemplate,
        BlueBandComponents
    },

    data: function(){
        return{
            listImagesForBlueBand:[
                        {
                            image: '-comics-digital-comics.png',
                            textImage: 'Digital comics'
                        },
                        {
                            image: '-comics-merchandise.png',
                            textImage: 'DC Merchandise'
                        },
                        {
                            image: '-comics-subscriptions.png',
                            textImage: 'subscription'
                        },
                        {
                            image: '-comics-shop-locator.png',
                            textImage: 'Comics shop locator'
                        },
                        {
                            image: '-dc-power-visa.svg',
                            textImage: 'DC power visa'
                        }
                    ],
                    
            dinamicComicsList:[
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                        "price": "$19.99",
                        "series": "Action Comics",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                        "price": "$3.99",
                        "series": "American Vampire 1976",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                        "price": "$16.99",
                        "series": "Aquaman",
                        "type": "graphic novel"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                        "price": "$2.99",
                        "series": "Batgirl",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                        "price": "$3.99",
                        "series": "Batman",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                        "price": "$2.99",
                        "series": "Batman Beyond",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                        "price": "$3.99",
                        "series": "Batman/Superman",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                        "price": "$4.99",
                        "series": "Batman/Superman Annual",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                        "price": "$5.99",
                        "series": "Batman: The Joker War Zone",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                        "price": "$6.99",
                        "series": "Batman: Three Jokers",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                        "price": "$4.99",
                        "series": "Batman: White Knight Presents: Harley Quinn",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                        "price": "$16.99",
                        "series": "Catwoman",
                        "type": "graphic novel"
                    }
            ]
        }
    }
}
</script>


<style scoped lang="scss">

main{
    position: relative;
    z-index: 50;
}
.posizionamento-elementi{
    max-width: 1200px;
    margin: 0 auto;
}

.black-band{
    background-image: url(../assets/jumbotron.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    height: 350px;    
}
.content-azzurro{
    height: 210px;
    background-color: rgb(0, 178, 238);
    display:flex
}
h1{
    color: white;
}

.content-container{
    display: flex;
    align-items: center;
}
.content-container-images{
    justify-content: center;
}
ul{
    display: flex;
    list-style: none;
}
.comics-container{
    height: 630px;
    background-color: rgb(24, 24, 24);
    color: white;
    padding-top: 55px;
}
.wrapper-comics{
    display: flex;
    flex-wrap: wrap;
}
.button-loader{
    padding: 10px;
    background-color: rgb(100, 100, 235);
    width: 15%;
    text-align: center;
    margin: 0 auto;
    margin-top: 43px;
}
.button-current-series{
    padding: 10px;
    background-color: rgb(100, 100, 235);
    width: 18%;
    text-align: center;
    font-size: bolder;
    font-weight: bold;
    font-size: 1.65rem;
    position: relative;
    bottom: 79px;
}
.button-loader a, .button-current-series a{
    text-decoration: none;
    color: white;
}
</style>
