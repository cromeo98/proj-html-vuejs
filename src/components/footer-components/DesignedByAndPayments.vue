<template>
  <div class="ms_bottom-footer">
    <div class="container clearfix">

      <!-- NEED TO FIX ALIGNMENT -->
      <!-- left-bot-footer -->
      <div class="float-start py-4">
        <p>
          <i class="far fa-copyright"></i>
          <span>
            2021 Landrick. Design with 
            <i class="fas fa-heart"></i> 
            by Shreethemes.
          </span>
        </p>
      </div>

      <!-- right bot-footer -->
      <div class="float-end py-4">
        <img class="px-1 ms_payment-icon" v-for="(payment, index) in payments" :key="index" :src="
          require(`../../assets/img/payment/${payment.name}.png`)
        " :alt="payment.alt">
      </div>


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

<style scoped lang="scss">

.ms_payment-icon{
  max-height: 25px;
}

</style>