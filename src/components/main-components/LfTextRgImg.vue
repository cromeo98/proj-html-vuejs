<template>
  <div id="jumbotron">
    <div class="ms_shorter-container">  
      <div class="container">
        <div class="row ms_red-bord align-items-center py-5">

          <aside class="col ms_blue-bord">
            <h5 class="ms_light-btn">Development</h5>
            <h2 class="ms_w-75x ms_title pt-1 pb-2">A Complete Developer Toolset</h2>
            <p class="ms_paragraph ms_grey-text pb-3">Launch your campaign and benefit from our expertise on designing and managing conversion centered bootstrap v5 html page.</p>

            <!-- button get startd -->
            <button class="ms_blue-btn me-3">Get Started</button>

            <!-- button documentation -->
            <button class="ms_white-btn">Documentation</button>

            <p class="ms_grey-text pt-3">Current Version: v3.5.0</p>

          </aside>
          <aside class="col text-center ms_blue-bord">
            <img src="../../assets/img/about.png" alt="developer avatar developing">
          </aside>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
export default {
    name: 'LfTextRgImg'
}
</script>

<style lang="scss" scoped>

#jumbotron{
  background-color: #f8f9fc;
  padding-bottom: 130px;
  padding-top: 50px;
}

.ms_light-btn{
  font-size: 0.75rem;
  border: 1px solid #d2daf5;
  text-align: center;
  border-radius: 15px;
  background-color: #e3e8f8;
  color: #2f55d4;
  display: inline-block;
  padding: 3px 8px;
  font-weight: 600;
}

.ms_title{
  font-size: 44px;
  font-weight: 700;
  line-height: 1.4;
}

.ms_paragraph{
  font-size: 17.5px;
}

</style>

