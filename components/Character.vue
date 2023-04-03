<template>
    <div class="person">  <!-- :style="backgroundUrl" -->
        <NuxtLink :to="'people/' + this.id">Voir</NuxtLink>
        <!-- <Btn :url="'people/' + persoObj.key" text= "Voir"/>  -->  
        <p></p>         
        <h5>{{ persoObj.name}}</h5>
    </div>
</template>

<script>
export default {
/*     data(){
        return{
            newName: "",             
        }
        
    }, */
    props: {
        persoObj:{
            type: Object
        },
        url:{
            type: String,
        },
        id:{
            type: Number,
        },
/*         name: {
            type: String, 
            required: true
        },
        firstname: {
            type: String
        },  */
        
    },
    methods:{
        
    },
    /* this.newName=this.name.replace(' ','-') ; */

/*     computed:{        
        backgroundUrl() {
        return  require('~/assets/images/characters/' + this.name.replace(' ','-') + '.jpg');
    }
    },  */

}
</script>

<style scoped>
    .person{
        text-align: center;
        max-width:200px;
        min-width:200px;
        max-height:200px;
        min-height:200px;
        border-radius: 100%;
        border: solid 2px yellow;
        background-position: center;
    }

    h4{
        color:white;
    }
</style>