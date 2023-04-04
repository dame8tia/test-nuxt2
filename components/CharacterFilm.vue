<template>
    <div>
        <span> {{ film }} </span>        
    </div>
</template>

<script>
export default{

    data() {
        return {
            filmInside:"",
        }
    },

    props:{
        numFilm:{
            type: Number
        },
        film:{
            type: String
        }
    },
    methods: {
        getSlug() {
        // Extrait l'ID du personnage à partir de l'URL de l'API
        const slugUrlParts = this.film.split('/');
        // console.log(slugUrlParts)
        /* return characterUrlParts[characterUrlParts.length - 2]; */
        }
    },

/*     async fetch() {
        let url= 'https://swapi.dev/api/films/' + this.numFilm;
        this.films = await fetch(url).then(res => res.json());
    }, */

}


</script>