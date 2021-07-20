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


        <div v-for="(keyfeaturesCard, index) in keyFeaturesCards" :key="index" class="col-3 ms_blue-bord p-4">

          <!-- posso trasformare la card in un componente? Sì, DA FARE IN FASE DI EDITING FINALE -->
          <div class="card-container ms_red-bord">
            
            <div><i :class="keyfeaturesCard.icon"></i></div>
            <div>{{keyfeaturesCard.title}}</div>
            <div>{{keyfeaturesCard.paragraph}}</div>

            <div>Read more</div> <!-- Read more uguale per tutti -->

          </div>

        </div>
      </div>

    </div>
  </section>
</template>

<script>
export default {
    name: 'LeftTitleWithParagAndFourCols',
    data (){
      return{
        keyFeaturesCards: [
          {
            icon: 'fas fa-layer-group',
            title: 'Modular',
            paragraph: 'Composed in a pseudo-Latin language which more or less corresponds.'
          },
          {
            icon: 'fas fa-desktop',
            title: 'Responsive',
            paragraph: 'Composed in a pseudo-Latin language which more or less corresponds.'
          },
          {
            icon: 'far fa-square',
            title: 'Customizable',
            paragraph: 'Composed in a pseudo-Latin language which more or less corresponds.'
          },
          {
            icon: 'fas fa-expand-arrows-alt',
            title: 'Scalable',
            paragraph: 'Composed in a pseudo-Latin language which more or less corresponds.'
          }
        ]
      }
    }
}
</script>

<style scoped lang="scss">

</style>