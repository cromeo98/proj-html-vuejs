<template>
  <section id="rates-section">
    <div class="ms_shorter-container">  
      <div class="container">

          <div class="row justify-content-center ms_red-bord">
            
            <div class="col-6 text-center ms_blue-bord mb-5">
            
              <h2 class="ms_section-titles">Our rates for developer from landrick team</h2>
            
              <p class="ms_grey-text">
                Start working with 
                <span class="ms_blue-bold-text">Landrick</span>
                that can provide everything you need to generate awareness, drive traffic, connect.
              </p>
            
            </div>
          
          </div>

          <div class="row justify-content-center ms_red-bord">

            <div v-for="(offer, index) in offers" :key="index" class="col-4 ms_blue-bord p-2">

              <div class="ms_offer-card-container p-4 ms_red-bord">

                <div class="ms_light-btn mb-3">{{offer.name}}</div>

                <div class="fs-2 fw-bold mb-2">${{offer.price}}</div>

                <div class="ms_grey-text mb-3">{{offer.isMonthly == true ? 'Per Month' : 'Per Year'}}</div>

                <div class="ms_grey-text">{{offer.description}}</div>

                <hr>

                <ul>
                  <li v-for="(privilege, index) in offer.privileges" :key="index" class="ms_grey-text mb-1">
                    <i class="far fa-check-circle ms_blue-text"></i>
                    <span class="ms_grey-text ms-2">{{privilege}}</span>
                  </li>
                </ul>

                <button class="ms_blue-btn w-100 me-3 mt-4 mb-3">Buy Now</button>

                <div class="ms_grey-text">{{offer.isMonthly == true ? '*No credit card required' : '*Credit card required'}}</div>
              
              </div>

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

<style lang="scss" scoped>

section{
  margin-top: 80px;

  ul>li{
    font-weight: 600;
  }
}

.ms_light-btn{
  border: 1px solid #d5ddf8;
  text-align: center;
  border-radius: 50px;
  background-color: #e3e8f8;
  color: #2f55d4;
  display: inline-block;
  padding: 6px 20px;
  font-weight: 600;
}

hr{
  background-color: #d1d2d3;
}

.ms_offer-card-container{
  border: 1px solid #f3f4f5;
  border-radius: 5px;
  box-shadow: 0px 2px 0px 2px #f3f4f5;
}

</style>