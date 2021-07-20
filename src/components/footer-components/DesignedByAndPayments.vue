<template>
  <div class="ms_bottom-footer">
    <div class="container clearfix py-4">
      <div class="float-start">
        <p>
          <i class="far fa-copyright"></i>
          <span>
            2021 Landrick. Design with 
            <i class="fas fa-heart"></i> 
            by Shreethemes.
          </span>
        </p>
      </div>
      <div class="float-end">rigth</div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'DesignedByAndPayments',
    data(){
      return{
        payments:[
          {
            name: 'american-ex',
            alt: 'american express payment'
          },
          {
            name: 'discover',
            alt: 'discover payment'
          },
          {
            name: 'master-card',
            alt: 'master card payment'
          },
          {
            name: 'paypal',
            alt: 'paypal payment'
          },
          {
            name: 'visa',
            alt: 'visa payment'
          }
        ]
      }
    }
}
</script>

<style>

</style>