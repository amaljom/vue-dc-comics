<template>
  <main>
    <!-- ci saranno due elementi nel main la fascia nera e quella azzurra -->
    <div class="container black-band">
        <div class="content-container posizionamento-elementi">
            <h1> Content goes here </h1>
        </div>
        <!-- div azzurro che poi dovò mettere in un altro component -->
        <div class="content-azzurro ">
            <div class="posizionamento-elementi content-container content-container-images">
                <ul>
                    <li v-for="(element,index) in listImagesForBlueBand" :key="index">
                        <img :src="element.image" alt="NON TROVATO">
                        <p class="text-style">text</p>
                    </li>
                    
                </ul>
            </div>
            
        </div>
    </div>
  </main>
</template>

<script>

export default{
    data: function(){
        return{
            listImagesForBlueBand:[
                
                        {
                            image: '../img/buy-comics-digital-comics.png'
                        },
                        {
                            image: '../img/buy-comics-merchandise.png'
                        },
                        {
                            image: '../img/buy-comics-subscriptions.png'
                        },
                        {
                            image: '../img/buy-comics-shop-locator.png'
                        },
                        {
                            image: '../img/buy-dc-power-visa.svg'
                        }
                       
                    ]
        }
    }
}

</script>


<style scoped lang="scss">

.black-band{
    background-color: rgb(26, 25, 25);
    height: 200px;
}
.content-azzurro{
    height: 250px;
    background-color: rgb(0, 178, 238);
}

h1{
    color: white;
}
.posizionamento-elementi{
    max-width: 1200px;
    margin: 0 auto;
}
.content-container{
    display: flex;
    align-items: center;
    height: 100%;
}

.content-container-images{
    justify-content: center;
}
ul{
    display: flex;
    list-style: none;
}
ul li{
    padding: 0 40px;
    display: flex;
    align-items: center;
}
img{
        width: 56px;
        height: 62px;
}
.text-style{
    font-size: 25px;
    color: white;
    padding-left: 15px;
}

</style>
