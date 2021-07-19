<template>
  <header>
    <div class="container">
      <div class="row">

        <!-- logo section  -->
        <div class="col-4">
          <img id="logo" src="../assets/img/logo-dark.png" alt="">
        </div>

        <!-- navbar section -->
        <div class="col-4">

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
        <div class="col-4">
          <ul>
            <li><i class="fas fa-search"></i></li>
            <li>
              <img id="settings-icon" src="../assets/img/settings-svg.svg"  alt="svg settings">
            </li>
            <li><i class="fab fa-github"></i></li>
            <li><svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" focusable="false" width="1em" height="1em" style="-ms-transform: rotate(360deg); -webkit-transform: rotate(360deg); transform: rotate(360deg);" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24"><path d="M15.71 12.71a6 6 0 1 0-7.42 0a10 10 0 0 0-6.22 8.18a1 1 0 0 0 2 .22a8 8 0 0 1 15.9 0a1 1 0 0 0 1 .89h.11a1 1 0 0 0 .88-1.1a10 10 0 0 0-6.25-8.19zM12 12a4 4 0 1 1 4-4a4 4 0 0 1-4 4z" fill="#626262"/></svg></li>
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

</style>
