<template>
    <section id="quick-start">
      <div class="shorter-container">
        <div class="container">

          <div class="row justify-content-center ms_red-bord">
            
            <div class="col-6 text-center ms_blue-bord">
            
              <h6 class="ms_blue-text pb-1">Quickstart</h6>
            
              <h2 class="ms_section-titles pb-1">Awesome isn't it? Let's dive in!</h2>
            
              <p class="ms_grey-text">
                Start working with 
                <span class="ms_blue-bold-text">Landrick</span>
                that can provide everything you need to generate awareness, drive traffic, connect.
              </p>
            
            </div>
          
          </div>

          <div class="row justify-content-center ms_red-bord">

            <div class="col-7 ms_blue-bord">

              <div class="ms_dynamic-panel ms_blue-bord p-4">

                <!-- al click di ognuno di questi bottoni apparirà un diverso testo nel <p> di sotto, quindi ancora una volta mi conviene creare un'array di oggetti nella quale inserire il "nome" dei bottoni e il testo associato -->
                <div class="ms_btn-container">
                  <button class="ms_my-dark-btn" :class="counter == index ? 'ms_active-btn' : ''" v-for="(button, index) in buttons" :key="index" @click="buttonIndexCounter(index)">{{button.name}}</button>
                </div>  
                

                <!-- questo p sarà da visualizzare come attivo solo quando il bottone corrispondente è attivo, quindi dobbiamo dargli una classe active quando l'index di un contatore che ora creo sarà uguale all'index del bottone -->
                <p class="ms_grey-text fw-bold" v-for="(button, index) in buttons" :key="index" :class="counter == index ? 'd-block' : 'd-none'">
                <span class="ms_green">{{button.key}}</span>  
                {{button.install}}
                <span class="ms_green">{{button.secKey}}</span>  
                {{button.fileName}}
                {{button.description}}
                </p>              

              </div>

              <div class="mt-3">
                <i class="far fa-check-circle ms_green"></i>
                <span class="ms_grey-text ms-2 me-5">Organize your data</span>
                <i class="far fa-check-circle ms_green"></i>
                <span class="ms_grey-text ms-2 me-5">Work with any team</span>
              </div>
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
            key: '$',
            install: ' npm install ',
            secKey: '-g',
            fileName: ' claps.js',
            description: ''          
          },
          {
            name: 'nuget',
            key: '',
            install: '',
            secKey: '',
            fileName: '',
            description: 'coming soon ...'          
          },
          {
            name: 'spm',
            key: '',
            install: '',
            secKey: '',
            fileName: '',
            description: 'coming soon ...'          
          },
          {
            name: 'github',
            key: '',
            install: '',
            secKey: '',
            fileName: '',
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

<style lang="scss" scoped>

section{
  margin-top: 100px;

  .ms_dynamic-panel{
    margin-top: 40px;
    background-color: #3c4858;
    border-radius: 5px;

      .ms_btn-container{
      border: 1px solid #626c78;
      background-color: #505b69;
      border-radius: 5px;

        .ms_my-dark-btn{
          width: 25%;
          padding: 7px 0;
          color: white;
          background-color: #505b69;
          border: none;
          border-radius: 5px;
          font-size: 20px;
        }
        .ms_active-btn{
          background-color: #3c4858;
        }
      }
    p{
      margin-bottom: 0;
      margin-top: 15px
    }
  }
}

</style>