<script>
export default {
  name: 'AppFooter'
}
</script>

<template>
    <footer>
        <!-- <div class="container"> -->
            <div class="row d-flex justify-content-between">
                <div class="col-auto mt-3 mx-auto mx-auto">
                    <NuxtLink to="/mentions-legales"> Mentions Légales </NuxtLink>
                    <!-- <a href="/mentions-legales">Lien Mentions légales</a> --> <!-- Avec un a on recharge la page, l'intérêt des balise NuxtLink est justement de ne pas recharger la page -->
                </div>
                <div class="col-auto mt-3 mx-auto mx-auto">
                    <NuxtLink to="/"> Codi'n Camp DWWM 2022-2023 </NuxtLink> 
                </div>
                <div class="col-auto mt-3 mx-auto mx-auto">
                    <NuxtLink to="/"> Nous retrouver </NuxtLink>
                </div>
            </div>
        <!-- </div> -->
    </footer>
</template>


<style>
footer{
    width: 100%;
    background-color: black;
/*     position: absolute;
    bottom:0; */
    /* margin-top:15vh; */
}
a{
    color: white;
    font-size:16px;
    
}

/* @media (min-width: 1024px) {

} */
</style>

