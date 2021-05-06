<template>
  <div>
    <v-container>
      <ProductHeader @sortYearChange="sortYearChanged($event)"></ProductHeader>
      <v-row>
        <product :products="products" v-for="(product, key) in filterdList" :key="key" :product="product"></product>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import Product from "./Product.vue";
import ProductHeader from "./ProductHeader.vue";
export default {
  name: "ProductList",
  components: { Product, ProductHeader },
  data: () => ({
    sortYear: "全て",
    products: [
      {
        id: 1,
        name: "work1",
        image: "../assets/works/dummyimage.png",
        year: "2020",
        category: "コーポレート",
        use: "html css JS",
      },
      {
        id: 2,
        name: "work2",
        image: "../assets/works/dummyimage.png",
        year: "2019",
        category: "LP",
        use: "Vue.js",
        info: "",
      },
      {
        id: 3,
        name: "work3",
        image: "../assets/works/dummyimage.png",
        year: "2018",
        category: "ECサイト",
        use: "デザイン",
      },
      {
        id: 4,
        name: "work4",
        image: "../assets/works/dummyimage.png",
        year: "2019",
        category: "LP",
        use: "Vue.js",
        info: "",
      },
    ],
  }),
  methods: {
    sortYearChanged: function(year) {
      this.sortYear = year;
    },
  },
  computed: {
    filterdList: function() {
      return this.products.filter((product, index) => {
        if (this.sortYear === "2020" && this.products[index].year === "2020") {
          return this.products[index];
        } else if (this.sortYear === "2019" && this.products[index].year === "2019") {
          return this.products[index];
        } else if (this.sortYear === "2018" && this.products[index].year === "2018") {
          return this.products[index];
        } else if (this.sortYear === "全て") {
          return this.products[index];
        }
      });
    },
  },
};
</script>
