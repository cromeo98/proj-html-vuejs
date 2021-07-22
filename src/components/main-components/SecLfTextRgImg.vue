<template>
  <section id="tools-and-documention">
    <div class="ms_shorter-container">  
      <div class="container">
        <div class="row ms_red-bord align-items-center py-5">

          <aside class="col-6 ms_blue-bord">
            <h2 class="ms_w-75x ms_section-titles pt-1 pb-2">Build tools and extensive documention</h2>
            <p class="ms_paragraph ms_grey-text pb-3">You can combine all the Landrick templates into a single one, you can take a component from the Application theme and use it in the Website.</p>

            <ul class="mb-3">
                <li v-for="(description, index) in descriptions" :key="index" class="mb-2">

                    <i class="far fa-check-circle ms_blue-text"></i>

                    <span class="ms_grey-text ms-2">{{description}}</span>

                </li>
            </ul>

            <button class="ms_blue-btn me-3">Read More</button>

          </aside>

          <aside class="col-6 text-center ms_blue-bord">
              <div>
                <img id="chart" src="../../assets/img/chart.png" alt="developer avatar developing">
              </div>

          </aside>
        </div>

      </div>
    </div>
  </section>
</template>

<script>
export default {
    name: 'SecLfTextRgImg',
    data(){
        return{
            descriptions: [
                'Digital Marketing Solutions for Tomorrow',
                'Our Talented & Experienced Marketing Agency',
                'Create your own skin to match your brand'
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

section{
    margin-top: 50px;
}

#chart{
    width: 80%;
}

</style>