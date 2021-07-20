<template>
  <section id="rates-section">
    <div class="container">

        <div class="row justify-content-center ms_red-bord">
          
          <div class="col-6 text-center ms_blue-bord">
          
            <h2>Our rates for developer from landrick team</h2>
          
            <p>
              <!-- questo <p> è comune a due sezioni (LeftTitleWithParagAndFourCols), posso formattarlo direttamente nel general.scss -->
              Start working with 
              Landrick <!-- questo sarà da inserire <strong> e blu --> 
              that can provide everything you need to generate awareness, drive traffic, connect.
            </p>
          
          </div>
        
        </div>

        <div class="row justify-content-center ms_red-bord">

          <div v-for="(offer, index) in offers" :key="index" class="col-4 ms_blue-bord">

            <div class="offer-card-container">

              <div>{{offer.name}}</div>

              <div>${{offer.price}}</div>

              <div>{{offer.isMonthly == true ? 'Per Month' : 'Per Year'}}</div>

              <div>{{offer.description}}</div>

              <hr>

              <ul>
                <li>{{offer.privileges[0]}}</li>
                <li>{{offer.privileges[1]}}</li>
                <li>{{offer.privileges[2]}}</li>
                <li>{{offer.privileges[3]}}</li>
                <li>{{offer.privileges[4]}}</li>
              </ul>

              <button>buy-now</button>

              <div>{{offer.isMonthly == true ? '*No credit card required' : '*Credit card required'}}</div>
            
            </div>

          </div>

        </div>

    </div>
  </section>
</template>

<script>
export default {
    name: 'CenterTitleWithParagAndThreeCols',
    data(){
      return {
        offers: [
          {
            name: 'Basic',
            price: '9.00',
            isMonthly: true,
            description: 'All the basics for businesses that are just getting started.',
            privileges: [
              'Full Access',
              'Enhanced Security',
              'Source Files',
              '1 Domain Free',
              'Enhanced Security'
            ],
            buyNowLink: '#',
            requiresCreditCard: false
          },
          {
            name: 'Business',
            price: '9.00',
            isMonthly: true,
            description: 'Better for growing businesses that want more customers.',
            privileges: [
              'Full Access',
              'Enhanced Security',
              'Source Files',
              '1 Domain Free',
              'Enhanced Security'
            ],
            buyNowLink: '#',
            requiresCreditCard: false
          },
          {
            name: 'Premium',
            price: '79.00',
            isMonthly: true,
            description: 'Advanced features for pros who need more customization.',
            privileges: [
              'Full Access',
              'Enhanced Security',
              'Source Files',
              '1 Domain Free',
              'Enhanced Security'
            ],
            buyNowLink: '#',
            requiresCreditCard: false
          }
        ]
      }
    }
}
</script>

<style>

</style>