<template>
  <div>
    <v-card 
      class="mx-10 elevation-5"
      max-width="auto"
    >
      <v-carousel
      class="my-5"
      cycle-false
      height="400"
      hide-delimiter-background
      show-arrows-on-hover
      >
        <v-carousel-item
          v-for="(slide, i) in slides"
          :key="i"
        >
          <v-sheet
            :color="colors[i]"
            height="100%"
          >
            <v-row
              class="fill-height"
            >
              <div class="text-h4">
                {{ slide }}
              </div>
            </v-row>
          </v-sheet>
        </v-carousel-item>
      </v-carousel>
    </v-card>
    
    <v-divider></v-divider>
    
    <v-data-table
      :headers="headers"
      :items="desserts"
      :items-per-page="5"
      class="elevation-5 mx-10 my-5 text-h3"
    ></v-data-table>
  </div>

</template>

<script>
export default {
  data () {
    return {
      headers: [
        {
          text: 'Sobremesa (Porção 100g)',
          align: 'start',
          sortable: false,
          value: 'name'
        },
        { text: 'Calorias', value: 'calories' },
        { text: 'Carboidratos (g)', value: 'carbs' },
        { text: 'gordura (g)', value: 'fat'},
        { text: 'Ferro (%)', value: 'iron'},
        { text: 'Proteína (g)', value: 'protein'}
      ],
      desserts: [
        {
          name: 'Iogurte de Morango',
          calories: '159',
          fat: 6.0,
          carbs: 24,
          protein: 4.0,
          iron: '1%',
        },
        {
          name: 'Éclair',
          calories: 262,
          fat: 16.0,
          carbs: 23,
          protein: 6.0,
          iron: '7%',
        },
        {
          name: 'Cupcake',
          calories: 305,
          fat: 3.7,
          carbs: 67,
          protein: 4.3,
          iron: '8%',
        },
      ],
      colors: [
        'green',
        'blue',
        'red',
        'yellow',
      ],
      slides:[
        `Olá! Seja bem vindo ao protótipo modelo de 
        tabelas. Aqui será exibida uma simples explicação
        sobre tabelas e também um exemplo padrão`,

        `As tabelas são componentes importantes 
        na área de desenvolvimento web devido às
        diversas aplicações onde elas podem ser 
        utilizadas`,

        `No exemplo abaixo, está sendo exibida uma
        tabela típica do ramo nutricional, construída
        encima de ferramentas de design mais minimalistas.
        Essa tabela possui a função de ter a sua
        organização de acordo com os valores das colunas.`,
        
        `Também é possível utilizar a ferramenta de
        paginação, presenta no canto inferior esquerdo
        da tabela para definir a quantidade de items a
        serem exibidos na tabela. Essa tabela, assim
        como todo este layout, foi construída com VueJS!`
      ]
    }
  }
}
</script>

<style>

.fill-height {
  display: flex;
  margin: auto; 
  padding: 10%;
  text-align: center;
  text-justify: auto;
}
</style>