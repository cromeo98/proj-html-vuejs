<template>
  <header>
    <div class="container">
      <div class="row ms_nav-container align-items-center ms_red-bord">

        <!-- logo section  -->
        <div class="col-3 ms_blue-bord">
          <img id="logo" src="../assets/img/logo-dark.png" alt="Landrick logo dark">
        </div>

        <!-- navbar section -->
        <div class="col-6 ms_blue-bord">

          <nav>
            <ul class="text-center">
              <li class="d-inline-block px-4" v-for="(navItem, index) in navItems" :key="index">

                <a class="text-uppercase" :href="navItem.link">{{navItem.name}}</a>

                <template v-if="navItem.type == 'dropdown'">
                  <i class="fas fa-chevron-down"></i>
                </template>                

              </li>
            </ul>
          </nav>

        </div>

        <!-- search and icons section  -->
        <div class="col-3 align-items-center ms_blue-bord">

          <ul class="d-flex">

            <li></li>
            <li></li>
            <li></li>
            <li></li>

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
        type: 'item',
        link: 'https://shreethemes.in/landrick/layouts/index.html'
        },
        {
        name: 'Landing',
        type: 'dropdown',
        link: '#'
        },
        {
        name: 'Pages',
        type: 'dropdown',
        link: '#'
        },
        {
        name: 'Docs',
        type: 'dropdown',
        link: '#'
        },
        {
        name: 'Demos',
        type: 'dropdown',
        link: '#'
        }
      ]
    }
  }
}
</script>


<style scoped lang="scss">

header{
  height: 74px;
}

.ms_nav-container{
  height: 74px;
  nav{
    a{
    color: #3c4858;
    font-size: 13px;
    font-weight: 700;
    }
    i{
      font-size: 13px;
      padding-left: 7px;
      color: #3c4858;
    }
  }

}

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
