<template>  

    <header >
        <div class="container-fluid">
        <div class="row d-flex justify-content-between">
            <div class="col-auto">
                <NuxtLink to="/" class="nav-link active" aria-current="page" >
                    <Logo />
                </NuxtLink>
            </div>

            <div class="col-auto">

                <nav class="navbar navbar-expand-lg bg-body-tertiary">
                    
                        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                            <span class="bi bi-list"></span>
                        </button>

                        <div class="collapse navbar-collapse" id="navbarSupportedContent">
                            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                                <li class="nav-item">
                                    <NuxtLink to="/" class="nav-link active" aria-current="page" >Accueil</NuxtLink>
                                </li>
                                <li class="nav-item">
                                    <NuxtLink to="/people" class="nav-link active">Personnages</NuxtLink>
                                </li>
                                <li class="nav-item dropdown">
                                    <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                                        Planètes
                                    </a>
                                </li>
                            </ul>
                            <form class="d-flex" role="search">
                                <input class="form-control me-2 text-warming" type="search" placeholder="Search" aria-label="Search">
                                <button class="btn btn-outline-success text-warming" type="submit">Recherche</button>
                            </form>
                        </div>
                    
                </nav>
            </div>
        </div>
        </div>
    </header>

</template>

<script>
    export default {
    name: 'AppHeader'
    }
</script>

<style scoped>

.navbar-toggler{
    border: solid 1px yellow;
}

.navbar-toggler-icon{
    color: yellow;
}

header{
    background-color: black;
}

</style>
