<template>
  <div class="container ms_top-footer">
      <div class="row ms_h-500px ms_red-bord">

          <!-- left-col -->
          <div class="col-3 ms_blue-bord gx-2">

              <!-- logo img -->
            <img id="logo-dark" src="../../assets/img/logo-light.png" alt="Landrick logo light">

            <!-- paragraph -->
            <p>
            Start working with Landrick that can provide everything you need to generate awareness, drive traffic, connect.    
            </p>

            <div class="ms_four-icons-container">
                <ul class="d-flex">
                    <li><i class="fab fa-facebook-f"></i></li>
                    <li><i class="fab fa-instagram"></i></li>
                    <li><i class="fab fa-twitter"></i></li>
                    <li><i class="fab fa-linkedin-in"></i></li>
                </ul>
            </div>
          </div>

          <!-- left-cen-col -->
          <div class="col-3 ms_blue-bord">
              <h3>Company</h3>
              <ul>

                  <!-- inserisco tanti <li> quanti sono gli oggetti presenti nell'array dei companyLinks -->
                  <li v-for="(companyLink, index) in companyLinks" :key="index">
                      <a :href="companyLink.link">{{companyLink.name}}</a>
                  </li>

              </ul>
          </div>

          <!-- right-cen-col -->
          <div class="col-3 ms_blue-bord">

              <h3>Usefull Links</h3>
              <ul>

                  <!-- inserisco tanti <li> quanti sono gli oggetti presenti nell'array dei companyLinks -->
                  <li v-for="(usefullLink, index) in usefullLinks" :key="index">
                      <a :href="usefullLink.link">{{usefullLink.name}}</a>
                  </li>

              </ul>
          </div>

          <!-- rigth-col -->
          <div class="col-3 ms_blue-bord"></div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'Informations',
    data (){
        return{
            companyLinks: [
                {
                    name: 'About us',
                    link: '#'
                },
                {
                    name: 'Services',
                    link: '#'
                },
                {
                    name: 'Team',
                    link: '#'
                },
                {
                    name: 'Pricing',
                    link: '#'
                },
                {
                    name: 'Project',
                    link: '#'
                },
                {
                    name: 'Carrers',
                    link: '#'
                },
                {
                    name: 'Blog',
                    link: '#'
                },
                {
                    name: 'Log in',
                    link: '#'
                },

            ],
            usefullLinks: [
                {
                    name: 'Terms of services',
                    link: '#'
                },
                {
                    name: 'Privacy Policy',
                    link: '#'
                },
                {
                    name: 'Documentation',
                    link: '#'
                },
                {
                    name: 'Changelog',
                    link: '#'
                },
                {
                    name: 'Components',
                    link: '#'
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">

.ms_top-footer{
    background-color: #202942;
    color: white;
}

#logo-dark{
    width: 134px;
}

.ms_four-icons-container{
    ul{
        padding-left: 0;
    }
}

</style>