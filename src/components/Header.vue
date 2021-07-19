<template>
  <header>
    <div class="container">
      <div class="row align-items-center">

        <!-- logo section  -->
        <div class="col-4">
          <img id="logo" src="../assets/img/logo-dark.png" alt="">
        </div>

        <!-- navbar section -->
        <div class="col-4 ms_cen-s">

          <nav class="navbar navbar-expand-lg navbar-light bg-light">

            <div class="container-fluid">

              <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">

                <span class="navbar-toggler-icon"></span>

              </button>

                <!-- start list of items (dropdown or not dropdown) in the navbar -->        
              <div class="collapse navbar-collapse" id="navbarSupportedContent">    
                   
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">

                  <!-- Qui ripeto tanti <li> quanti sono gli elementi presenti nell'array di oggetti navItems e assegno la classe "dropdown" -->
                  <li v-for="(navItem, index) in navItems" :key="index" class="nav-item" :class="navItems[index].type == 'item' ? '' : 'dropdown'">
                    <template v-if="navItems[index].type == 'item'">
                      <a class="nav-link active" aria-current="page" href="#">{{navItems[index].name}}</a>
                    </template>
                    <template v-else>
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                      {{navItems[index].name}}
                    </a>
                    <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
                      <li><a class="dropdown-item" href="#">Action</a></li>
                      <li><a class="dropdown-item" href="#">Another action</a></li>
                      <li><hr class="dropdown-divider"></li>
                      <li><a class="dropdown-item" href="#">Something else here</a></li>
                    </ul>
                    </template>
                  </li>

                </ul>
              </div>
            </div>
          </nav>

        </div>

        <!-- search and icons section  -->
        <div class="col-4 ms_right-s align-items-center">
          <ul class="d-flex">
            <li class="px-1"><i class="fas fa-search"></i></li>
            <li class="px-1">
              <img id="settings-icon" src="../assets/img/settings-svg.svg"  alt="svg settings">
            </li>
            <li class="px-1"><i class="fab fa-github"></i></li>
            <li class="px-1">
              <img id="user-icon" src="../assets/img/user.svg"  alt="svg user">
              </li>
          </ul>
        </div>

      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {

      // Lista degli elementi da inserire nella NavBar
      navItems: [
        {
        name: 'Home',
        type: 'item'
        },
        {
        name: 'Landing',
        type: 'dropdown'
        },
        {
        name: 'Pages',
        type: 'dropdown'
        },
        {
        name: 'Docs',
        type: 'dropdown'
        },
        {
        name: 'Demos',
        type: 'dropdown'
        },
      ]
    }
  }
}
</script>


<style scoped lang="scss">

#logo{
  width: 134px;
}

#settings-icon, #user-icon{
  width: 16px;
}

li>i{
  font-size: 16px;
}

</style>
