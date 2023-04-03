<template>
    <main>
        <h1 class="" >{{ perso }}</h1>
        <!-- <h1 class="" >{{ perso.results[slug].name }}</h1> -->
        <div class="title text-center text-center">            
            <img class="image shadow-lg shadow-color mb-5 bc-yellow rounded" src="@/assets/images/nasa-accueil.jpg" alt="">
        </div>

        <h2 class="title text-warning text-center">Carte d'identité</h2>
        <div class="cartId row d-flex justify-content-around align-items-center" >
            
            <div class="col-auto cartIdCol border border-warning me-3">
                <p>Nom :                    <span>{{ perso.name }}</span>               </p>
                <p>Année de naissance :     <span>{{ perso.birth_year }}</span>         </p>
                <p>Planète de naissance :   <a :href="perso.homeworld">{{ perso.homeworld }}</a></p>
                <p>Genre :                  <span>{{ perso.genre }}</span>              </p>
                <p>Espèce :                 <span v-for="i in perso.species.length" :esp="perso.species[i]">{{ perso.species.length}}</span>            </p>
                
            </div>
            <div class="col-auto cartIdCol border border-warning ms-3">
                <p>Taille :                 <span>{{ perso.height }}</span> cm </p>
                <p>Poids :                  <span>{{ perso.mass }}</span> Kg  </p>
                <p>Couleur des cheveux :    <span>{{ perso.hair_color }}</span>  </p>
                <p>Couleur de la peau:      <span>{{ perso.skin_color }}</span>  </p>
                <p>Couleur des yeux :       <span>{{ perso.eye_color }}</span>   </p>

            </div>
        </div>

        <h2 class="title text-warning text-center">Filmographie</h2>
        <div class="row d-flex justify-content-center align-items-center mx-5 mt-5">   
            <img v-for="episode in apparition"
                class="col-auto" 
                :src="require(`~/assets/images/movies/${episode.name}.jpg`)" 
                :alt="`${episode.name}`"
                width="150px"
                height="200px"
            >
        </div>
    </main>
</template>

<script>
    export default {
        props:{
            id:{
                type: Number,
            },
            _slug:{
                type: Number,
            }
        },
        data(){
            return {
            "apparition": [
                    {
                        "name": "episode01", 
                    },
                    {
                        "name": "episode02", 
                    },
                    {
                        "name": "episode03", 
                    },
                    {
                        "name": "episode06", 
                    }
                ],
            "perso": [], 
            }
        },

        async asyncData({ params }) {
            const slug = params.slug // When calling /abc the slug will be "abc"
            return { slug }
        },

        async fetch() {
            let url= 'https://swapi.dev/api/people/' + this.$route.params.slug;
            this.perso = await fetch(url).then(res => res.json());
        },
        mounted(){ 
            console.log(this.$route.params.slug)
        }
    }
</script>


<style scoped>
    main {
        min-height:100%;
        background-color: rgb(0, 0, 0);
        color: rgb(243, 172, 7);
    }

    .image{
        width: 250px;
        height:250px;
        box-shadow: -5px 5px 5px 0px rgba(244, 169, 58, 0.79);
    }

    .cartIdCol{
        min-width: 400px;
        margin:15px 15px 15px 15px;
    }

    @media (min-width: 576px) {
        .title{
            text-align: start;
        }
    }

</style>