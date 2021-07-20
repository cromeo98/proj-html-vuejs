<template>
    <section id="quick-start">

      <div class="container">

        <div class="row justify-content-center ms_red-bord">
          
          <div class="col-6 text-center ms_blue-bord">
          
            <h5>Quickstart</h5>
          
            <h2>Awesome isn't it? Let's dive in!</h2>
          
            <p>
              <!-- questo <p> è comune a due sezioni (LeftTitleWithParagAndFourCols), posso formattarlo direttamente nel general.scss -->
              Start working with 
              Landrick <!-- questo sarà da inserire <strong> e blu --> 
              that can provide everything you need to generate awareness, drive traffic, connect.
            </p>
          
          </div>
        
        </div>

        <div class="row justify-content-center ms_red-bord">

          <div class="col-7 ms_blue-bord">

            <div class="ms_dynamic-panel">

              <!-- al click di ognuno di questi bottoni apparirà un diverso testo nel <p> di sotto, quindi ancora una volta mi conviene creare un'array di oggetti nella quale inserire il "nome" dei bottoni e il testo associato -->
              <button v-for="(button, index) in buttons" :key="index" @click="buttonIndexCounter(index)">{{button.name}}</button>

              <!-- questo p sarà da visualizzare come attivo solo quando il bottone corrispondente è attivo, quindi dobbiamo dargli una classe active quando l'index di un contatore che ora creo sarà uguale all'index del bottone -->
              <p v-for="(button, index) in buttons" :key="index" :class="counter == index ? 'd-block' : 'd-none'">{{button.description}}</p>              

            </div>
          </div>

        </div>
      
      </div>
  </section>
</template>

<script>
export default {
    name: 'CenterTitleWithParagAndPanel',
    data(){
      return{
        buttons:[
          {
            name: 'npm',
            description:  '$ npm install -g claps.js'
          },
          {
            name: 'nuget',
            description: 'coming soon ...' 
          },
          {
            name: 'spm',
            description: 'coming soon ...'
          },
          {
            name: 'github',
            description: 'coming soon ...' 
          }       
        ],
        counter: 0
      }
    },
    methods:{
      buttonIndexCounter(button){
        this.counter = button;
      }
    }
}
</script>

<style>

</style>