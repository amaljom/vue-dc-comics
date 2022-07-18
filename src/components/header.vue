<template>
<!-- CREO UN DIV DOVE METTERE L'HEADER -->
<!-- ALL' INTERNO DI ESSO CREO DUE DIV CONTENTI RISPETTIVAMENTE LOGO E LA LISTA -->
  <header>
        <nav class="navbar">
            <!-- logo -->
            <div>
                <img src="../assets/dc-logo.png" alt="Non trovato">
            </div>
            <!-- lista -->
            <div>
                <ul>
                    <li v-for="(element,index) in listElementForNavbar" :key="index">
                       <a @click.prevent :href="element.url"> {{ element.text }}</a>
                    </li>
                </ul>
            </div>
        </nav>
  </header>
</template>

<script>

export default{
    data: function(){
        return{
            listElementForNavbar:[
                        {
                            text: 'CHARACTERS',
                            url:'#'
                        },
                        {
                            text: 'COMICS',
                            url:'#'
                        },
                        {
                            text: 'MOVIES',
                            url:'#'
                        },
                        {
                            text: 'TV',
                            url:'#'
                        },
                        {
                            text: 'GAMES',
                            url:'#'
                        },
                        {
                            text: 'COLLECTIBLES',
                            url:'#'
                        },
                        {
                            text: 'VIDEOS',
                            url:'#'
                        },
                        {
                            text: 'FANS',
                            url:'#'
                        },
                        {
                            text: 'NEWS',
                            url:'#'
                        },
                        {
                            text: 'SHOP',
                            url:'#'
                        }
                    ]
        }
    }
}
   
</script>


<style lang="scss" scoped>

.navbar{
    display: flex;
    justify-content: space-around;
    max-width: 1500px;
    margin: 0 auto;
    align-items: center;
}

ul{
    padding: 43px;
}
ul li{
    display: inline;
    list-style: none;
    padding: 1rem;
    font-size: 0.9rem;
    font-weight: bolder;
    padding: 41px 13px;
    &:hover{
        border-bottom: solid 2px rgb(83, 83, 233);
    }
}
li a{
    text-decoration: none;
    color:black;
}

img{
width: 80px;
}

</style>