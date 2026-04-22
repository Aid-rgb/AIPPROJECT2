<template>
  <v-container>
    <v-row justify="center">
      <v-col cols="12" md="10">
        <v-card class="mt-5" elevation="2">
          <!-- Картинка -->
          <v-img 
            src="https://images.unsplash.com/photo-1558981403-c5f9899a28bc?q=80&w=1000&auto=format&fit=crop" 
            height="400px" 
            cover
          ></v-img>
          
          <!-- Текст -->
          <v-card-text>
            <h1 class="text--primary mb-3">Harley Davidson Sportster S</h1>
            <p>
              Мощный и агрессивный. Двигатель Revolution Max 1250T, 
              121 л.с., жидкостное охлаждение. Легкая алюминиевая рама, 
              премиальная подвеска Showa. Стиль Street Performance...
            </p>
          </v-card-text>

          <!-- Кнопки -->
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn color="warning">Edit</v-btn>
            <v-btn color="success">Buy</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {}
  }
}
</script>