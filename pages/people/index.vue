<template>

<main>
    <h1>Listing des personnages</h1>
    <div class="container px-4 text-center">
        <div class="row d-flex justify-content-center align-items-center">
            <Character class="col-3 m-3" v-for="(perso, index) in personnages.results" :key="index" :persoObj="perso" :id="index+1" /> <!-- :name=name -->
            <!-- <Character class="col-3 m-3" v-for="(perso, index) in personnages.results" :index= "index" :name= "perso.name"  /> -->
        </div>
            <!-- {{ personnages.results}}  -->
            <!-- {{ personnages.results[0].name }} -->
            <!-- <pre>
            {{ personnages.results[0].name }}    
            url="name: people-slug, params:{ slug:index }" 
            /pre> -->
    </div>
</main>

</template>

<script>
    export default {
    /*     mounted() {
        }, */
        data(){
            return {
            "personnages": []
                /* { "name": "John", "lastname": "Doe"  },*/               
            }
        },
        async fetch() {
/*             let url = "https://swapi.dev/api/people/";

            while(url){// On boucle ensuite sur l'url
                const response = await fetch(url).then(res => res.json());
                url = response.next;
                this.personnages = this.personnages.concat(response.results);
            } */

            this.personnages = await fetch(
                'https://swapi.dev/api/people/'
            ).then(res => res.json());

            //console.log(this.personnages);
    }
}
</script>

<style scoped>
    main {
        background-color: black;
        color: white;
    }
</style>

