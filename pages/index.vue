<template>
  
  <main>
    <div class="container-fluid">

      <div class="title d-flex">
        <p>Retrouvez l'univers de Star Wars</p>
      </div>

      <div class="accueil-princ">

        <div class="fond">                    
        </div> 

        <div class="icones">
          <div class="row d-flex justify-content-center align-items-center"> 
          
            <div class="col-sm-4">
              <div class="link-perso d-flex justify-content-center align-items-center mx-auto">
                <NuxtLink to="/" class="mx-auto link-vaisseau">
                  <div class="icone-vaisseaux">
                  </div>  
                </NuxtLink>
              </div>                     
            </div>

            <div class="col-sm-4">              
              <div class="link-perso d-flex justify-content-center align-items-center mx-auto">
                <NuxtLink to="/people" class="mx-auto">
                  <div class="icone-perso">
                  </div>   
                </NuxtLink>
              </div>           
            </div>

            <div class="col-sm-4"> 
              <NuxtLink to="/people" class="mx-auto">
                <div class="icone-galaxy link-perso ">
                </div>  
              </NuxtLink>                        
            </div>  

          </div>                 
        </div>
        
      </div>      

    </div> 

<!--     <div id="carouselExampleControls" class="carousel slide" data-bs-ride="carousel">
      <div class="carousel-inner w-100">
        <div class="carousel-item active">
          <img src="..." class="d-block w-100" alt="...">
        </div>
        <div class="carousel-item">
          <img src="..." class="d-block w-100" alt="...">
        </div>
        <div class="carousel-item">
          <img src="..." class="d-block w-100" alt="...">
        </div>
      </div>
      <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
      </button>
      <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </button>
    </div> -->
  </main>

</template>

<script>

  export default {
    name: 'IndexPage',
  }

</script>

<style scoped>

  main{
    width: 100%;
    margin: 0;
    padding: 0;
    background-color: rgb(0, 0, 0);
    color: white;
  }

  .container{
    width: 100%;
    height: 100%;
  }

  .link-perso:hover{
    cursor: pointer;
  }
  .link-vaisseau{
    margin-right:0 !important;
  }
  .title{
    width: 200px;
    margin-left:75px;
    margin-top:-120px;
    flex-wrap: wrap;
    color: yellow;
    font-size: xx-large;
  }

  .accueil-princ{    
    /* width:100vw; */ /* A supprimer ?  */
    height:70vh;   
    position:relative; 
    content:"";
  }

  .fond{
    position:absolute;
    left:0;
    top:10%;
    width: 100%;
    height:80%;
    background-image: url("~assets/images/equipe.png"); /* nasa-accueil.jpg */
    background-size: contain;
    background-position: center;
    background-repeat: no-repeat;
    background-color: rgb(0, 0, 0);
    border: solid 1px yellow;
    opacity: 0.3;
    content: ""
  }

  .icones{
    position:relative;
    top: 180px;
  }

  .icone-galaxy{

    float: left;

    width: 70px;
    height: 70px;

    border: solid 2px yellow;
    border-radius: 50%;    

    background-image: url("~assets/images/AccueilLesGalaxies.jpg");
    background-size: cover;
    background-position: center;
  }

  .icone-perso{

    width: 70px;
    height: 70px;

    border: solid 2px yellow;
    border-radius: 50%;  

    background-image: url("~assets/images/Dark-Vador.jpg");
    background-size: cover;
    background-position: center;
  }

  .icone-vaisseaux{
    float: right;

    width: 70px;
    height: 70px;

    border: solid 2px yellow;
    border-radius: 50%;  

    background-image: url("~assets/images/AccueilLesVaisseaux.jpg");
    background-size: cover;
    background-position: center;
  }

  @media (min-width: 576px) {
  .icone-galaxy{
    width: 110px;
    height: 110px;
    
  }
  .icone-perso{
    width: 110px;
    height: 110px;

    position: relative;
    top:150px;
    
  }
  .icone-vaisseaux{
    width: 110px;
    height: 110px;
    
  }

  .row{
    transition: all ease 0.2s;
  }
 
  }

</style>

