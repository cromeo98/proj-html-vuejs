<template>
  <section id="register-user">
    <div class="container">
      <div class="row justify-content-center ms_red-bord">

        <!-- title and paragraph -->
        <div class="col-6 text-center ms_blue-cord">
          <h2>Want to be among the first to find out?</h2>

          <p>
            <!-- questo <p> è comune a tre sezioni (LeftTitleWithParagAndFourCols), posso formattarlo direttamente nel general.scss -->
            Start working with 
            Landrick <!-- questo sarà da inserire <strong> e blu --> 
            that can provide everything you need to generate awareness, drive traffic, connect.
          </p>
        </div>

      </div>
      
      <div class="row justify-content-center ms_red-bord">
        <!-- register form -->
        <div class="col-6 text-center ms_form-container ms_blue-cord">

          <input type="text" placeholder="E-mail :">
          <button>Get Started</button>

        </div>

      </div>
    </div>
  </section>
</template>

<script>
export default {
    name: 'RegisterUser'
}
</script>

<style scoped lang="scss">

</style>