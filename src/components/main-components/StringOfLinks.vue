<template>
  <section id="string-of-logos" class="ms_blue-bord">

    <div class="ms_shorter-container">
      <div class="container">
        <div class="row py-5 justify-content-between ms_red-bord">
        
            <div class="col-2 text-center" v-for="(stringImage, index) in stringImages" :key="index">
        
              <img class="ms_logo-string-img" :src="
                require(`../../assets/img/stringImgs/${stringImage.name}.svg`)
              " :alt="stringImage.alt">
        
            </div>
        
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

section{
  background-color: #f8f9fc;
  border-top: 1px solid #eef0f3;
  margin-top: 130px;
}

.ms_logo-string-img{
  max-height: 25px;
}

</style>