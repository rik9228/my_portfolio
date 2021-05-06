<template>
  <div>
    <Header></Header>
    <v-main>
      <v-parallax dark src="@/assets/img_0346.jpg">
        <v-row align="center" justify="center">
          <v-col class="text-center" cols="12">
            <h1 class="display-1 font-weight-thin mb-4">My PORTFOLIO</h1>
            <h4 class="subheading">my portfolio</h4>
          </v-col>
        </v-row>
      </v-parallax>
      <v-container class="pb-16">
        <h2 class="headline font-weight-bold text-center my-16">
          WORKS
        </h2>
        <ProductList></ProductList>
      </v-container>
      <v-container>
        <section class="section">
          <div class="inner">
            <div class="section-title-block">
              <h2 class="headline font-weight-bold text-center my-16">
                ABOUT
              </h2>
            </div>
            <v-row>
              <v-col cols="12" sm="12" md="4" lg="6">
                <v-card class="mx-auto">
                  <v-card-text>
                    <v-card-subtitle style="padding-left:0;">WEB Designer</v-card-subtitle>
                    <p class="display-1 text--primary">
                      森下 陸
                    </p>
                    <p>age:23</p>
                    <div class="text--primary">
                      - 何事にも、全力で。
                    </div>
                  </v-card-text>
                  <v-card-actions>
                    <v-btn text color="orange accent-4" to="about">
                      READ MORE
                    </v-btn>
                  </v-card-actions>
                </v-card>
              </v-col>
              <v-col cols="12" sm="12" md="8" lg="6"><img src="@/assets/profile.jpg" alt="" width="100%"/></v-col>
            </v-row>
          </div>
        </section>
      </v-container>
      <v-container>
        <section class="section">
          <div class="inner">
            <div class="section-title-block">
              <h2 class="headline font-weight-bold text-center my-16">
                CONTACT
              </h2>
              <p class="section-desc text-center">
                お問合わせは下記からご連絡をください。
              </p>
            </div>
            <div class="contact-wrapper">
              <div class="contact-list">
                <v-row class="text-center">
                  <v-col>
                    <v-btn depressed x-large color="primary">
                      Primary
                    </v-btn>
                  </v-col>
                </v-row>
              </div>
            </div>
          </div>
        </section>
      </v-container>
    </v-main>
  </div>
</template>
<script>
import Header from "../components/Header.vue";
import ProductList from "../components/ProductList.vue";

export default {
  name: "Home",
  components: {
    Header,
    ProductList,
  },
};
</script>
