<template>
  <section id="key-features">

    <div class="container">
    
      <div class="row ms_red-bord">
    
        <div class="col-12">
    
          <h2>Key Features</h2>
          <p>
            Start working with 
            Landrick <!-- questo sarà da inserire <strong> e blu --> 
            that can provide everything you need to generate awareness, drive traffic, connect.
          </p>
    
        </div>
    
      </div>
    
      <div class="row ms_red-bord">


        <div class="col-3">

          <!-- da ICON a PARAGRAPH prendo gli elementi da un array, così da risparmiare codice perchè ripeterò la col-3 con un v-for-->
          <div>ICON</div>
          <div>TITLE</div>
          <div>PARAGRAPH</div>

          <div>Read more</div> <!-- Read more uguale per tutti -->

        </div>
      </div>

    </div>
  </section>
</template>

<script>
export default {
    name: 'LeftTitleWithParagAndFourCols'
}
</script>

<style>

</style>