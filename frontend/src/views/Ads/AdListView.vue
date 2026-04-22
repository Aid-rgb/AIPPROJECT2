<template>
  <v-container>
    <v-row justify="center">
      <v-col cols="12" sm="8" lg="6">
        <h1 class="text--secondary mb-3 mt-3">My ads</h1>

        <v-card
          v-for="ad in ads"
          :key="ad.id"
          class="mb-3"
          max-width="1000"
          elevation="2"
        >
          <v-row no-gutters>
            <!-- Картинка -->
            <v-col cols="12" md="4">
              <v-img :src="ad.src" height="175px" cover></v-img>
            </v-col>
            
            <!-- Текст и кнопка -->
            <v-col cols="12" md="8">
              <v-card-title class="text-h5">{{ ad.title }}</v-card-title>
              <v-card-text style="height: 85px; overflow: hidden; text-overflow: ellipsis;">
                {{ ad.desc }}
              </v-card-text>
              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn color="primary" variant="text" :to="'/ad/' + ad.id">
                  Open
                </v-btn>
              </v-card-actions>
            </v-col>
          </v-row>
        </v-card>

      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      ads: [
        {
          title: "Sportster S",
          desc: "Классический круизер с двигателем Revolution Max 1250T и агрессивным дизайном",
          promo: true,
          src: "https://picsum.photos/seed/harley1/800/400",
          id: "1"
        },
        {
          title: "Fat Boy",
          desc: "Легендарный байк с цельнолитыми дисками, низким профилем и атмосферой свободы",
          promo: true,
          src: "https://picsum.photos/seed/harley2/800/400",
          id: "2"
        },
        {
          title: "Road King",
          desc: "Идеален для дальних путешествий с ветровым стеклом, кофрами и круиз-контролем",
          promo: true,
          src: "https://picsum.photos/seed/harley3/800/400",
          id: "3"
        },
        {
          title: "Street Glide",
          desc: "Туринговый мотоцикл с премиальной аудиосистемой, Apple CarPlay и максимальным комфортом",
          promo: true,
          src: "https://picsum.photos/seed/harley4/800/400",
          id: "4"
        }
      ]
    }
  }
}
</script>