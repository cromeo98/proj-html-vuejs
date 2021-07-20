<template>
  <section id="string-of-logos">

    <div class="container">
      <div class="row py-5 justify-content-between">
      
          <div class="col-2" v-for="(stringImage, index) in stringImages" :key="index">
      
            <img class="ms_logo-string-img" :src="
              require(`../../assets/img/stringImgs/${stringImage.name}.svg`)
            " :alt="stringImage.alt">
      
          </div>
      
      </div>
    </div>
  
  </section>


</template>

<script>
export default {
    name: 'StringOfLinks',
    data(){
      return{
        stringImages:[
          {
            name: 'amazon',
            alt: 'amazon image'
          },
          {
            name: 'google',
            alt: 'google image'
          },
          {
            name: 'lenovo',
            alt: 'lenovo image'
          },
          {
            name: 'paypal',
            alt: 'paypal image'
          },
          {
            name: 'shopify',
            alt: 'shopify image'
          },
          {
            name: 'spotify',
            alt: 'spotify image'
          }
        ]
      }
    }
}
</script>

<style scoped lang="scss">

.ms_logo-string-img{
  max-height: 25px;
}

</style>