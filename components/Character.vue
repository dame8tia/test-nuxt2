<template>
    <main>
        <div class="text-center">
            <NuxtLink :to="'people/' + this.id">
                <h5>{{ persoObj.name}}</h5>
            </NuxtLink>
        </div>
        <div class="person" :style="{ backgroundImage: `url(${persoObj.image})` }">  <!-- :style="backgroundUrl" -->
        </div>
    </main>
    
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
            return this.persoObj.image;
        /* return  require('~/assets/images/characters/' + this.name.replace(' ','-') + '.jpg');
    }
    },  */

}
</script>

<style scoped>
    .person{
        text-align: center;
        max-width:180px;
        min-width:180px;
        max-height:180px;
        min-height:180px;
        border-radius: 100%;
        border: solid 2px yellow;
        background-position: center;
        background-size:  cover;
    }

    h5{
        color:rgb(255, 255, 255);
    }

    
</style>