<template>
  <v-col cols="12" sm="6" md="4" lg="4">
    <v-card>
      <v-img class="white--text align-end" height="200px" src="https://dummyimage.com/250x150/000/fff">
        <v-card-title class="text--white">
          <div>{{ product.name }}</div>
        </v-card-title>
      </v-img>

      <v-card-subtitle class="pb-0">{{ product.year }}</v-card-subtitle>

      <v-card-text class="text--primary">
        <div>カテゴリー：{{ product.category }}</div>
        <div>使用言語,ツール：{{ product.use }}</div>
        <div>その他：{{ product.info }}</div>
      </v-card-text>

      <v-card-actions>
        <v-btn color="orange" text>
          LINK
        </v-btn>
      </v-card-actions>
    </v-card>
  </v-col>
</template>

<script>
export default {
  name: "Product",
  props: {
    product: {
      require: true,
    },
  },
};
</script>
