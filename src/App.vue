<template>
  <div>
    <nav class="navbar navbar-light navbar-expand-lg fixed-top" id="mainNav">
        <div class="container"><a class="navbar-brand">V8</a><button data-toggle="collapse" data-target="#navbarResponsive" class="navbar-toggler" aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation"><i class="fa fa-bars"></i></button>
            <div
                class="collapse navbar-collapse" id="navbarResponsive">
                <!-- MENU DE NAVEGACION -->
                <ul class="nav navbar-nav ml-auto" id="menu-v8">
                    <li class="nav-item" role="presentation">
                      <!-- REEMPLAZAR CON ELEMENTO ROUTER LINK A CON RUTA NOMBRADA -->
                      <!-- <a href="/">portada</a> -->
                      <router-link :to="{name: 'index'}">Inicio</router-link>
                    </li>
                    <li class="nav-item" role="presentation">
                      <!-- REEMPLAZAR CON ELEMENTO ROUTER LINK A CON RUTA NOMBRADA -->
                      <!-- <a href="/sobremi">sobre mí</a> -->
                      <router-link :to="{name: 'about'}">Sobre Mi</router-link>
                    </li>
                    <li class="nav-item" role="presentation">
                      <!-- REEMPLAZAR CON ELEMENTO ROUTER LINK A CON RUTA ESTÁTICA -->
                      <!-- <a href="/contacto">contacto</a>  -->
                      <router-link :to="{name: 'contact'}">Contacto</router-link>
                    </li>
                    <li class="nav-item" role="presentation">
                      <!-- REEMPLAZAR CON ELEMENTO ROUTER LINK A RUTA ESTÁTICA -->
                      <!-- <a href="/post/1">último post</a> -->
                      <router-link to="/post/1/articulo">Post</router-link>
                    </li>
                    <li class="nav-item" role="presentation">
                      <!-- REEMPLAZAR CON ELEMENTO ROUTER LINK A RUTA ESTÁTICA -->
                      <!-- <a href="/post/1">último post</a> -->
                      <router-link to="administrador/simple">Admin</router-link>
                    </li>
                </ul>
        </div>
        </div>
    </nav>
    <!-- ROUTER VIEW QUE CARGARÁ LAS VISTAS (INICIO, SOBRE MÍ, CONTACTO, ETC.) -->
    <transition name='my-transition'>
        <router-view></router-view>
    </transition>
  </div>
  
</template>

<script>
export default {

}
</script>

<style scoped>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;  
}
#menu-v8 a{
  text-shadow: 1px 1px #000;
}

.my-transition-enter-active, .my-transition-leave-active {
  transition: .3s;
}
 
.my-transition-enter-active {
  transition-delay: .3s;
}
 
.my-transition-enter, .my-transition-leave-active {
  opacity: 0
}

</style>
