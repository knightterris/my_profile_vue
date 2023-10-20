<template>
    <v-app class="gradient-black">
        <slot></slot>
       
        <v-bottom-navigation grow class="pure-black text-white" style="position: fixed; bottom: 0; width: 100%; z-index:99;">
            <v-btn value="recent">
                <v-icon>mdi-history</v-icon>
                <span>Recent</span>
            </v-btn>

            <v-btn value="favorites">
                <v-icon>mdi-heart</v-icon>
                <span>Favorites</span>
            </v-btn>

            <v-btn value="nearby">
                <v-icon>mdi-map-marker</v-icon>
                <span>Nearby</span>
            </v-btn>

            <v-btn value="more" @click.stop="drawer = !drawer">
                <v-icon>mdi-menu</v-icon>
                <span>More</span>
            </v-btn>
        </v-bottom-navigation>

        <hr class="break-line">

        <v-footer class="bg-transparent text-white">
          <v-row>
            <!-- First Column: Social Media Icons -->
            <v-col cols="12" lg="4"  md="4" sm="12">
              <div class="text-center my-4">
                <p class="subtitle-1">You can reach me via:</p>
              </div>
              <div class="d-flex justify-center">
                <v-btn icon class="mx-4">
                  <v-icon size="24" @click="goWebsite('github')">mdi-github</v-icon>
                </v-btn>
                <v-btn icon class="mx-4" @click="goWebsite('instagram')">
                  <v-icon size="24">mdi-instagram</v-icon>
                </v-btn>
                <v-btn icon class="mx-4" @click="goWebsite('facebook')">
                  <v-icon size="24">mdi-facebook</v-icon>
                </v-btn>
                <v-btn icon class="mx-4" @click="goWebsite('linkedin')">
                  <v-icon size="24">mdi-linkedin</v-icon>
                </v-btn>
              </div>
            </v-col>

        <!-- Second Column: Contact Information -->
          <v-col cols="12" lg="4"  md="4" sm="12" class="mt-5">
            <ul class="text-center contact-line">
              <li class="d-flex">
                <v-icon size="30" class="mx-4">mdi-email</v-icon>
                <p>agkaungmyat19@gmail.com</p>
              </li>
              <li class="d-flex">
                <v-icon size="30" class="mx-4">mdi-phone</v-icon>
                <p>+959 791 385 988</p>
              </li>
              <li class="d-flex">
                <v-icon size="30" class="mx-4">mdi-map-marker</v-icon>
                <p>Thuwunna ,Yangon ,Myanmar</p>
              </li>
            </ul>
          </v-col>

          <!-- Third Column: NGL Link -->
          <v-col cols="12" lg="4"  md="4" sm="12">
            <div class="d-flex">
              <v-btn icon @click="goWebsite('ngl')" class="mx-5">
                <v-icon size="24">mdi-link</v-icon>
              </v-btn>
              <p class="mt-3">NGL</p>
            </div>
          </v-col>
        </v-row>

        <!-- Copyright Text -->
      </v-footer>
        <v-row>
          <v-col cols="12" lg="12"  md="12" sm="12" class="text-center text-white mt-5">
            <p class="caption">Copyright © 2023 Aung Kaung Myat</p>
          </v-col>
        </v-row>

      <hr class="invisible-line">
        <v-navigation-drawer v-model="drawer" temporary class="gradient-black text-white">
          <v-list>
            <v-list-item to="/about-me">
              <v-list-item-avatar class="d-flex">
        
                <v-icon class="me-3">mdi-account</v-icon>
                <v-list-item-title>About Me</v-list-item-title>
              </v-list-item-avatar>
            </v-list-item>

            <v-list-item to="/github">
              <v-list-item-avatar class="d-flex">
                <v-icon class="me-3">mdi-github</v-icon>
                <v-list-item-title>GitHub</v-list-item-title>
              </v-list-item-avatar>
            </v-list-item>

            <v-list-item to="/linkedin">
              <v-list-item-avatar class="d-flex">
                <v-icon class="me-3">mdi-linkedin</v-icon>
                <v-list-item-title>LinkedIn</v-list-item-title>
              </v-list-item-avatar>
            </v-list-item>
          </v-list>
        </v-navigation-drawer>

        
    </v-app>
</template>

<script>
export default {
  name: "LayoutPage",
  data: () => ({
      drawer: false,
      group: null,
  }),

  watch: {
    group () {
      this.drawer = false
    },
  },
  methods: {
    goWebsite(webName){
      const website = webName;
      switch (website) {
        case "github":
          window.open("https://github.com/knightterris", "_blank");
        break;
        case "instagram":
          window.open("https://instagram.com/k_is_heree", "_blank");
        break;
        case "linkedin":
          window.open("https://www.linkedin.com/in/aung-kaung-myat-072762275", "_blank");
        break;
        case "facebook":
          window.open("https://www.facebook.com/profile.php?id=100010977960543&mibextid=ZbWKwL", "_blank");
        break;
        case "ngl":
          window.open("https://ngl.link/k_is_here1", "_blank");
        break;
      
        default:
          break;
      }
    }
  },
};
</script>

<style scoped>
.gradient-black{
    background: linear-gradient(to bottom, #3c3c3c, #000);
}
.pure-black{
  background: #000;
}
.break-line{
  background: #ffffff;
  height: 2px;
  margin: 100px 1px;
}
.invisible-line{
  margin: 100px 1px;
  background: #000 !important;
}
.v-btn--elevated{
  color: #000;
}
.contact-line{
  line-height: 3;
}
.contact-line>li{
  align-items: center;
}
</style>
