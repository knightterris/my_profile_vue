<template>
  <Layout>
    <v-container>
      <!-- name section -->
      <v-row class="first-row">
        <v-col cols="12" md="6">
          <!-- Text content on the left -->
          <div class="text-content">
            <h2  class="text-white my-4 animate__animated animate__fadeInUpBig" id="name">I'm Aung Kaung Myat</h2>
            <p  class="text-white mb-4 animate__animated animate__fadeInUpBig animate__delay-1s">I'm a 
                <span>Web developer</span>
            </p>
            <p  class="text-white mb-4 animate__animated animate__fadeInUpBig animate__delay-2s">As a junior web developer, I bring passion, creativity, and a commitment to excellence to every project I undertake.</p>
            <h3  class="text-white animate__animated animate__fadeInUpBig animate__delay-3s nosifer-font">Unleash Your Vision with ME.</h3>
          </div>
        </v-col>
      </v-row>

      <!-- about me section -->
      <v-row>
        <v-col cols="12" sm="12" md="12" lg="6" class="d-flex align-center mb-4">
          <v-text class="text-white animate__animated animate__fadeInUpBig animate__delay-4s pa-5" >
            I am a well-motivated, energetic Junior Web Developer with a strong passion for web development.
            With a hunger for learning and a commitment to staying updated with the latest industry trends, I am always eager to explore new technologies and expand my skill set.
            I am excited to work alongside clients who share my passion for innovation.
            Let's collaborate and bring your vision to life! 
          </v-text>
        </v-col>
        <v-col cols="12" sm="12" md="12" lg="6" class="mb-4">
          <v-img class="rounded-circle animate__animated animate__fadeInUpBig animate__delay-5s" aspect-ratio="1/1" width="400" height="400" cover  src="@/assets/images/pf.jpg"></v-img>
        </v-col>
        <v-col cols="12" sm="12" md="12" lg="12" class="d-flex justify-end mt-5">
          <v-btn color="blue" dark text class="mx-3" @click="goWebsite('github')">
            <v-icon left class="mr-3">
              mdi-github
            </v-icon>
            GitHub
          </v-btn>
          <v-btn color="blue" dark text class="mx-3" @click="goWebsite('about')">
            <v-icon left class="mr-3">
              mdi-account
            </v-icon>
            About Me
          </v-btn>
        </v-col>
      </v-row>
      <!-- flexing section -->
      <v-row>
        <v-col cols="12" lg="12" md="12" sm="12" class="text-white text-center my-3">
          <h3 class="my-3">
            What I Do
          </h3>
        </v-col>
      </v-row>

      <v-row>
        <v-col cols="12" lg="3" md="6" sm="12" class="my-3 text-white pa-3">
          <v-card class="text-center" text="Fast" variant="">
            <v-row align="center">
              <v-col>
                <v-icon size="50">mdi-lightning-bolt-outline</v-icon>
              </v-col>
            </v-row>
            <v-row align="center">
              <v-col>
                <p>Fast load times and lag free interaction, my highest priority.</p>
              </v-col>
            </v-row>
          </v-card>
        </v-col>

        <v-col cols="12" lg="3" md="6" sm="12" class="my-3 text-white pa-3">
          <v-card class="text-center" text="Creative" variant="">
            <v-row align="center">
              <v-col>
                <v-icon size="50">mdi-lightbulb-on</v-icon>
              </v-col>
            </v-row>
            <v-row align="center">
              <v-col>
                <p>Crafted with passion. Embrace the extraordinary. Dare to be different.</p>
              </v-col>
            </v-row>
          </v-card>
        </v-col>

        <v-col cols="12" lg="3" md="6" sm="12" class="my-3 text-white pa-3">
          <v-card class="text-center" text="Dynamic" variant="">
            <v-row align="center">
              <v-col>
                <v-icon size="50">mdi-rocket-launch</v-icon>
              </v-col>
            </v-row>
            <v-row align="center">
              <v-col>
                <p>Websites don't have to be static - Let's transform your website into a vibrant and interactive platform that leaves a lasting impression on your audience. </p>
              </v-col>
            </v-row>
          </v-card>
        </v-col>

        <v-col cols="12" lg="3" md="6" sm="12" class="my-3 text-white pa-3">
          <v-card class="text-center" text="Satisfaction" variant="">
            <v-row align="center">
              <v-col>
                <v-icon size="50">mdi-hand-heart</v-icon>
              </v-col>
            </v-row>
            <v-row align="center">
              <v-col>
                <p>Meet your satisfaction. Collaborate to bring your vision to life, flawlessly tailored to your desires. </p>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
      </v-row>

      <!-- projects section -->

      <v-row>
        <v-col cols="12" lg="4" md="6" sm="12" class="my-3 pa-3">
          <v-card class="mx-auto gradient-black  text-white " max-width="344">
            <v-img src="@/assets/images/bethany.gif" height="200px" cover ></v-img>
            <v-card-title>
              Bethany
            </v-card-title>
            <v-card-subtitle>
              A duly licensed agency & training center
            </v-card-subtitle>
            <v-card-actions>
              <v-btn color="orange-lighten-2" variant="text" @click="goWebsite('bethany')">
                Explore
              </v-btn>
              <v-spacer></v-spacer>
              <v-btn :icon="show ? 'mdi-chevron-up' : 'mdi-chevron-down'" @click="show = !show"></v-btn>
            </v-card-actions>
            <v-expand-transition>
              <div v-show="show">
                <v-divider></v-divider>
                <v-card-text>
                  I actively participated in the implementation of CRUD operations, contributing to the development of these processes. I also conducted thorough analyses of any bug errors that arose and provided valuable assistance in troubleshooting alongside senior developers.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>

        <v-col cols="12" lg="4" md="6" sm="12" class="my-3 pa-3">
          <v-card class="mx-auto gradient-black  text-white " max-width="344">
            <v-img src="@/assets/images/royalac.gif" height="200px" cover ></v-img>
            <v-card-title>
              Royal Aircon
            </v-card-title>
            <v-card-subtitle>
              An air-con service Group
            </v-card-subtitle>
            <v-card-actions>
              <v-btn color="orange-lighten-2" variant="text" @click="goWebsite('royalac')">
                Explore
              </v-btn>
              <v-spacer></v-spacer>
              <v-btn :icon="show ? 'mdi-chevron-up' : 'mdi-chevron-down'" @click="show = !show"></v-btn>
            </v-card-actions>
            <v-expand-transition>
              <div v-show="show">
                <v-divider></v-divider>
                <v-card-text>
                  I actively participated in the implementation of CRUD operations, contributing to the development of these processes. I also conducted thorough analyses of any bug errors that arose and provided valuable assistance in troubleshooting alongside senior developers.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
        
        <v-col cols="12" lg="4" md="6" sm="12" class="my-3 pa-3">
          <v-card class="mx-auto gradient-black  text-white " max-width="344">
            <v-img src="@/assets/images/grandwinner.gif" height="200px" cover ></v-img>
            <v-card-title>
              Grand Winner
            </v-card-title>
            <v-card-subtitle>
              An air-con service Group
            </v-card-subtitle>
            <v-card-actions>
              <v-btn color="orange-lighten-2" variant="text" @click="goWebsite('grandWinner')">
                Explore
              </v-btn>
              <v-spacer></v-spacer>
              <v-btn :icon="show ? 'mdi-chevron-up' : 'mdi-chevron-down'" @click="show = !show"></v-btn>
            </v-card-actions>
            <v-expand-transition>
              <div v-show="show">
                <v-divider></v-divider>
                <v-card-text>
                  I actively participated in the implementation of CRUD operations, contributing to the development of these processes. I also conducted thorough analyses of any bug errors that arose and provided valuable assistance in troubleshooting alongside senior developers.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>

        <v-col cols="12" lg="4" md="6" sm="12" class="my-3 pa-3">
          <v-card class="mx-auto gradient-black  text-white " max-width="344">
            <v-img src="@/assets/images/mkm.gif" height="200px" cover ></v-img>
            <v-card-title>
              Moe Kaung Myay (Wordpress)
            </v-card-title>
            <v-card-subtitle>
              A Book Shop
            </v-card-subtitle>
            <v-card-actions>
              <v-btn color="orange-lighten-2" variant="text" @click="goWebsite('mkm')">
                Explore
              </v-btn>
              <v-spacer></v-spacer>
              <v-btn :icon="show ? 'mdi-chevron-up' : 'mdi-chevron-down'" @click="show = !show"></v-btn>
            </v-card-actions>
            <v-expand-transition>
              <div v-show="show">
                <v-divider></v-divider>
                <v-card-text>
                  I changed the html template, written by a frontend developer, of this site to wordpress structure and develop as well as maintained it.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>

        <v-col cols="12" lg="4" md="6" sm="12" class="my-3 pa-3">
          <v-card class="mx-auto gradient-black  text-white " max-width="344">
            <v-img src="@/assets/images/mmz.gif" height="200px" cover ></v-img>
            <v-card-title>
              Artist Moe Myint Zaw (Wordpress)
            </v-card-title>
            <v-card-subtitle>
              A portfolio website of an artist
            </v-card-subtitle>
            <v-card-actions>
              <v-btn color="orange-lighten-2" variant="text" @click="goWebsite('mmz')">
                Explore
              </v-btn>
              <v-spacer></v-spacer>
              <v-btn :icon="show ? 'mdi-chevron-up' : 'mdi-chevron-down'" @click="show = !show"></v-btn>
            </v-card-actions>
            <v-expand-transition>
              <div v-show="show">
                <v-divider></v-divider>
                <v-card-text>
                  I changed the html template, written by a frontend developer, of this site to wordpress structure and develop as well as maintained it.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>

        <v-col cols="12" lg="4" md="6" sm="12" class="my-3 pa-3">
          <v-card class="mx-auto gradient-black  text-white " max-width="344">
            <v-img src="@/assets/images/pandaaircon.gif" height="200px" cover ></v-img>
            <v-card-title>
              Panda Aircon(Wordpress)
            </v-card-title>
            <v-card-subtitle>
              An air-con service Group
            </v-card-subtitle>
            <v-card-actions>
              <v-btn color="orange-lighten-2" variant="text" @click="goWebsite('pandaAc')">
                Explore
              </v-btn>
              <v-spacer></v-spacer>
              <v-btn :icon="show ? 'mdi-chevron-up' : 'mdi-chevron-down'" @click="show = !show"></v-btn>
            </v-card-actions>
            <v-expand-transition>
              <div v-show="show">
                <v-divider></v-divider>
                <v-card-text>
                  I took part in toggling the Myanmar and English languages of the website with javascript and helped adjust some of the designs.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>

        <v-col cols="12" lg="4" md="6" sm="12" class="my-3 pa-3">
          <v-card class="mx-auto gradient-black  text-white " max-width="344">
            <v-img src="@/assets/images/topcomet.gif" height="200px" cover ></v-img>
            <v-card-title>
              TopComet (Wordpress)
            </v-card-title>
            <v-card-subtitle>
              An overseas employing Agency
            </v-card-subtitle>
            <v-card-actions>
              <v-btn color="orange-lighten-2" variant="text" @click="goWebsite('topcomet')">
                Explore
              </v-btn>
              <v-spacer></v-spacer>
              <v-btn :icon="show ? 'mdi-chevron-up' : 'mdi-chevron-down'" @click="show = !show"></v-btn>
            </v-card-actions>
            <v-expand-transition>
              <div v-show="show">
                <v-divider></v-divider>
                <v-card-text>
                  I took part in adjusting some of the designs.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>

        <v-col cols="12" lg="4" md="6" sm="12" class="my-3 pa-3">
          <v-card class="mx-auto gradient-black  text-white " max-width="344">
            <v-img src="@/assets/images/sms.gif" height="200px" cover ></v-img>
            <v-card-title>
              School Management System
            </v-card-title>
            <v-card-subtitle>
              A school management system
            </v-card-subtitle>
            <v-card-actions>
              <v-btn color="orange-lighten-2" variant="text" @click="goWebsite('sms')">
                Explore
              </v-btn>
              <v-spacer></v-spacer>
              <v-btn :icon="show ? 'mdi-chevron-up' : 'mdi-chevron-down'" @click="show = !show"></v-btn>
            </v-card-actions>
            <v-expand-transition>
              <div v-show="show">
                <v-divider></v-divider>
                <v-card-text>
                  I developed this website with laravel and made the database design by myself. But this website is not hosted yet.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>

        <v-col cols="12" lg="4" md="6" sm="12" class="my-3 pa-3">
          <v-card class="mx-auto gradient-black  text-white " max-width="344">
            <v-img src="@/assets/images/multitaskapp.gif" height="200px" cover ></v-img>
            <v-card-title>
              Multi-task App
            </v-card-title>
            <v-card-subtitle>
              A multi-tasking web app
            </v-card-subtitle>
            <v-card-actions>
              <v-btn color="orange-lighten-2" variant="text" @click="goWebsite('multi')">
                Explore
              </v-btn>
              <v-spacer></v-spacer>
              <v-btn :icon="show ? 'mdi-chevron-up' : 'mdi-chevron-down'" @click="show = !show"></v-btn>
            </v-card-actions>
            <v-expand-transition>
              <div v-show="show">
                <v-divider></v-divider>
                <v-card-text>
                  I developed this website with laravel and made the database design by myself. But this website is not hosted yet.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>

        <v-col cols="12" lg="4" md="6" sm="12" class="my-3 pa-3">
          <v-card class="mx-auto gradient-black  text-white " max-width="344">
            <v-img src="@/assets/images/lovecalc.gif" height="200px" cover ></v-img>
            <v-card-title>
              LoveCalculator
            </v-card-title>
            <v-card-subtitle>
              A lovecalculator Game
            </v-card-subtitle>
            <v-card-actions>
              <v-btn color="orange-lighten-2" variant="text" @click="goWebsite('lovecalc')">
                Explore
              </v-btn>
              <v-spacer></v-spacer>
              <v-btn :icon="show ? 'mdi-chevron-up' : 'mdi-chevron-down'" @click="show = !show"></v-btn>
            </v-card-actions>
            <v-expand-transition>
              <div v-show="show">
                <v-divider></v-divider>
                <v-card-text>
                  I developed this with VueJs.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
      </v-row>

      <v-row>
        <v-col cols="12" lg="12" md="12" sm="12">
          <v-card class="gradient-black text-white">
            <v-tabs
              v-model="tab"
              align-tabs="center"
            >
              <v-tab value="one">Web</v-tab>
              <v-tab value="two">UI/UX</v-tab>
              <v-tab value="three">Branding</v-tab>
            </v-tabs>

            <v-card-text>
              <v-window v-model="tab">
                <v-window-item value="one">
                  <v-card variant="">
                    <h4 class="text-center service-headers">Everywhere & Every Device, Your Site Should Flow Seamlessly</h4>
                    <ul class="ul-li-lines">
                      <li>Custom website development tailored to your goals.</li>
                      <li>Responsive and mobile-friendly designs.</li>
                      <li>Seamless integration of UI/UX designs.</li>
                      <li>Performance optimization for fast loading times.</li>
                      <li>CMS implementation for easy content management.</li>
                    </ul>
                  </v-card>
                </v-window-item>

                <v-window-item value="two">
                  <v-card variant="">
                    <h4 class="text-center service-headers">It’s All About the User Experience</h4>
                    <ul class="ul-li-lines">
                      <li>A visually appealing and user-friendly website.</li>
                      <li>Intuitive and user-centric interface designs.</li>
                      <li>
                        Wireframing and prototyping for seamless user experiences.
                      </li>
                      <li>Visual design that reflects your brand identity.</li>
                      <li>Information architecture and navigation optimization.</li>
                    </ul>
                  </v-card>
                </v-window-item>

                <v-window-item value="three">
                  <v-card variant="">
                    <h4 class="text-center service-headers">Your Brand Identity Should Be Stamped On All You Do</h4>
                    <ul class="ul-li-lines">
                      <li>
                        Maximize the potential of your website with our strategic
                        marketing expertise.
                      </li>
                      <li>
                        Our website marketing strategies are designed to maximize
                        your online presence and drive meaningful results.
                      </li>
                      <li>
                        We offer a range of services to enhance your website's
                        performance and visibility.
                      </li>
                      <li>
                        Create and optimize compelling content to engage and
                        captivate your audience.
                      </li>
                      <li>Gain visibility in search engines.</li>
                    </ul>
                  </v-card>
                </v-window-item>
              </v-window>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>

<!-- dummy  -->
<!-- 2405 scroll length -->
<!-- dummy -->
    </v-container>
    
  </Layout>
</template>

<script>
import Layout from './LayoutPage.vue';
export default {
  name: 'HomePage',
  data() {
    return {
      scrollLength: 0,
      show: false,
      tab:null,
    }
  },
  components: {
    Layout,
  },
  created() {
    window.addEventListener("scroll", this.scrollWatch);
  },
  beforeUnmount () {
    window.removeEventListener("scroll", this.scrollWatch);
  },
  methods: {
    scrollWatch() {
      var scrollLength = window.scrollY;
      console.log("Scroll Length: " + scrollLength + " pixels");
      this.scrollLength = scrollLength;
    },
    goWebsite(webName){
      const website = webName;
      switch (website) {
        case "about":
          this.$router.push("/about");
        break;
        case "github":
          window.open("https://github.com/knightterris", "_blank");
        break;
        case "bethany":
          window.open("http://bethany.com.mm/", "_blank");
        break;
        case "royalac":
          window.open("http://royalaircon.hmmdemo.com", "_blank");
        break;
        case "grandWinner":
          window.open("http://grandwinner.com.mm/", "_blank");
        break;
        case "mkm":
          window.open("https://moekaungmyay.com/", "_blank");
        break;
        case "mmz":
          window.open("https://artistmoemyintzaw.com/", "_blank");
        break;
        case "pandaAc":
          window.open("http://pandaairconmyanmar.com/", "_blank");
        break;
        case "topcomet":
          window.open("http://topcomet.com.mm/", "_blank");
        break;
        case "sms":
          window.open("https://github.com/knightterris/School-Management-System", "_blank");
        break;
        case "multi":
          window.open("https://github.com/knightterris/multi-task-app", "_blank");
        break;
        case "lovecalc":
          window.open("https://funlovecalculator.vercel.app/", "_blank");
        break;
        default:
          break;
      }
    },
  },
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Nosifer&display=swap');
.gradient-black{
    background: linear-gradient(to bottom, #3c3c3c, #000);
}
.text-content {
  padding: 20px;
}

.pf{
  width: 400px;
  height: 400px;
}
.nosifer-font{
  font-family: 'Nosifer', sans-serif;
  /* font-size: 20px; */
}
.ul-li-lines{
  line-height: 3;
  font-size: 15px;
}
.service-headers{
  line-height:2;
  font-size:15px;
}
/* Add styles for your circular picture here */
</style>
