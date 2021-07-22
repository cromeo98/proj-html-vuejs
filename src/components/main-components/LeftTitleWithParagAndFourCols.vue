<template>
  <section id="key-features">

    <div class="ms_shorter-container">
    
      <div class="row ms_red-bord">
    
        <div class="col-12">
    
          <h2 class="ms_section-titles">Key Features</h2>

          <!-- questo <p> è comune a due sezioni (centertitlewithparagandpanel), posso formattarlo direttamente nel general.scss -->
          <p class="w-50 ms_grey-text">
            Start working with 
            <span class="ms_blue-bold-text">Landrick</span>
            that can provide everything you need to generate awareness, drive traffic, connect.
          </p>
    
        </div>
    
      </div>
    
      <div class="row ms_red-bord">


        <div v-for="(keyfeaturesCard, index) in keyFeaturesCards" :key="index" class="col-3 pt-5 ms_blue-bord">

          <!-- posso trasformare la card in un componente? Sì, DA FARE IN FASE DI EDITING FINALE -->
          <div class="ms_card-container">
            
            <div class="ms_icon-container"><i :class="keyfeaturesCard.icon"></i></div>
            <div class="ms_darkgrey-text ms_subtitle mb-3">{{keyfeaturesCard.title}}</div>
            <div class="ms_grey-text mb-3">{{keyfeaturesCard.paragraph}}</div>

            <a href="#" class="ms_blue-text">Read more<i class="fas fa-chevron-right ps-2"></i></a> <!-- Read more uguale per tutti -->

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

section{
  margin-top: 130px;
}

.ms_card-container{
  padding: 20px;
  border: 1px solid #f4f5f6;
  border-radius: 5px;
  box-shadow: 0px 0px 3px 1px #f4f5f6;
}

.ms_icon-container{
  width: 60px;
  height: 60px;
  line-height: 60px;
  text-align: center;
  border-radius: 5px;
  background-color: #e9edfb;
  color: #2f55d4;
  font-size: 22px;
  margin-bottom: 25px;
}

.ms_subtitle{
  font-size: 18px;
  font-weight: 600;
}

a{
  i{
    vertical-align: middle;
    font-size: 12px;
  }
}

</style>