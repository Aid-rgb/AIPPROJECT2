<template>
  <div>
    <!-- CAROUSEL -->
    <v-container fluid>
      <v-row>
        <v-col cols="12">
          <v-carousel
            height="350px"
            hide-delimiter-background
            show-arrows-on-hover
          >
            <v-carousel-item
              v-for="ad in promoAds"
              :key="ad.id"
              :src="ad.src"
              cover
            >
              <div class="ad-link">
                <v-btn
                  class="error"
                  :to="'/ad/' + ad.id"
                >
                  {{ ad.title }}
                </v-btn>
              </div>
            </v-carousel-item>
          </v-carousel>
        </v-col>
      </v-row>
    </v-container>

    <!-- GRID -->
    <v-container class="mt-5">
      <v-row>
        <v-col
          cols="12"
          md="6"
          lg="3"
          v-for="ad in ads"
          :key="ad.id"
        >
          <v-card class="mx-auto" elevation="5">
            <v-img
              :src="ad.src"
              height="200px"
              cover
            ></v-img>

            <v-card-title class="text-h6">
              {{ ad.title }}
            </v-card-title>

            <v-card-text>
              {{ ad.desc }}
            </v-card-text>

            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn
                color="primary"
                variant="text"
                :to="'/ad/' + ad.id"
              >
                Open
              </v-btn>
              <v-btn
                color="success"
                variant="flat"
              >
                Buy
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
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
          src: "https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=800",
          id: "1"
        },
        {
          title: "Fat Boy",
          desc: "Легендарный байк с цельнолитыми дисками, низким профилем и атмосферой свободы",
          promo: true,
          src: "https://images.unsplash.com/photo-1449426468159-d96dbf08f19f?w=800",
          id: "2"
        },
        {
          title: "Road King",
          desc: "Идеален для дальних путешествий с ветровым стеклом, кофрами и круиз-контролем",
          promo: true,
          src: "https://images.unsplash.com/photo-1568772585301-64d3a34c0860?w=800",
          id: "3"
        },
        {
          title: "Street Glide",
          desc: "Туринговый мотоцикл с премиальной аудиосистемой, Apple CarPlay и максимальным комфортом",
          promo: true,
          src: "https://images.unsplash.com/photo-1615117970016-573d8a5e64a7?w=800",
          id: "4"
        }
      ]
    };
  },
  computed: {
    promoAds() {
      return this.ads.filter((ad) => ad.promo === true);
    }
  }
};
</script>

<style scoped>
.ad-link {
  position: absolute;
  bottom: 50px;
  left: 50%;
  background: rgb(0, 0, 0, 0.5);
  transform: translate(-50%, 0);
  padding: 5px 15px;
  border-top-right-radius: 5px;
  border-top-left-radius: 5px;
}
</style>