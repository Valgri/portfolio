<template>
  <div>
    <main>
      <Leftbar />
      <Rightbar />
    </main>
    <v-card height="70">
      <v-footer absolute class="font-weight-medium">
        <v-col class="text-center" cols="12" md="6">
          <vue-typed-js
            :strings="['with Vue CLI', 'by Valeriy H']"
            :typeSpeed="150"
            :backSpeed="100"
            :backDelay="300"
            :loop="true"
          >
            <h3>
              {{ new Date().getFullYear() }} — Portflio created
              <span class="typing"></span>
            </h3>
          </vue-typed-js>
        </v-col>
<!--        <v-col cols="12" md="6" class="end-cl">-->
<!--          <v-btn-->
<!--            v-for="(icon, i) in icons"-->
<!--            :key="i"-->
<!--            class="mx-10"-->
<!--            icon-->
<!--            :href="icon.link"-->
<!--            target="_blank"-->
<!--            rel="noopener"-->
<!--            aria-label="social buttons"-->
<!--          >-->
<!--            <v-icon size="40px">{{ icon.item }}</v-icon>-->
<!--          </v-btn>-->
<!--        </v-col>-->
      </v-footer>
    </v-card>
  </div>
</template>

<script>
import Leftbar from "./components/Leftbar";
import Rightbar from "./components/Rightbar";
export default {
  name: "App",

  components: {
    Leftbar,
    Rightbar,
  },

  data: () => ({
    icons: [
      {
        item: "mdi-telegram",
        link: "https://t.me/webmark_tl",
      },
      {
        item: "mdi-github",
        link: "https://github.com/Valgri",
      },
    ],
  }),
};
</script>
<style>
@import url(https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Montserrat:ital,wght@0,700;1,400&display=swap);
.inner {
  background-position: 50%;
  background-repeat: no-repeat;
  background-size: contain;
  height: inherit;
  position: relative;
  box-shadow: inset 0 -190px 80px -110px rgba(50, 50, 50, 0.35),
    inset 0 190px 80px -110px rgba(50, 50, 50, 0.35);
}
.wraper {
  height: calc(100vh - 70px);
}
.slick-arrow {
  color: red;
}
.slick-dots li button:before {
  font-size: 18px;
  color: #837888;
  opacity: 0.75;
}
.slick-dots li.slick-active button:before {
  color: #bf4442;
  opacity: 1;
}
.slick-dots {
  bottom: 30px;
}

.right {
  padding: 0 20px;
  width: 30%;
  height: 100%;
  display: flex;
  align-items: center;
  flex-direction: column;
}
.right .slick-arrow {
  color: red;
}
.slider {
  width: 70%;
  height: inherit;
  position: relative;
  overflow: hidden;
}
body {
  font-family: Montserrat, sans-serif;
}
h1 {
  font-size: 36px;
  padding: 50px 0 100px 0;
  font-weight: 700;
  -webkit-mask-image: linear-gradient(
    -75deg,
    rgba(0, 0, 0, 0.6) 30%,
    #000 50%,
    rgba(0, 0, 0, 0.6) 70%
  );
  -webkit-mask-size: 200%;
  animation: shine 3s infinite;
  /* text-shadow: -1px -1px #778086, 2px 2px 0 #000; */
}
@-webkit-keyframes shine {
  from {
    -webkit-mask-position: 150%;
  }

  to {
    -webkit-mask-position: -50%;
  }
}
h1,
h2 {
  line-height: 120%;
  text-align: center;
}
h2 {
  font-size: 24px;
  padding: 0 0 50px 0;
}
h3,
main {
  color: #3e454a;
}
main {
  height: calc(100vh - 70px);
  display: flex !important;
  background-color: #fbf9f9;
}
img,
main {
  max-width: 100%;
}
img {
  height: auto;
}
.theme--light.v-footer {
  background-color: #fbf9f9 !important;
}
.v-sheet.v-footer:not(.v-sheet--outlined) {
  box-shadow: 0 0 3px 1px rgba(0, 0, 0, 0.2), 0 0 0 0 rgba(0, 0, 0, 0.14),
    0 0 0 0 rgba(0, 0, 0, 0.12) !important;
}
.mx-10 {
  margin: 0 10px;
}
.end-cl {
  display: flex;
  justify-content: flex-end;
}
.v-btn:before {
  width: 115%;
}
.theme--light.v-btn.v-btn--icon:hover {
  color: #bf4442;
}
.slick-active {
  z-index: 100000;
}
@media screen and (max-width: 1024px) {
  main {
    flex-direction: column-reverse;
  }
  .v-footer {
    flex-direction: column-reverse;
    justify-content: center;
  }
  .end-cl {
    justify-content: center;
  }
  .col-md-6 {
    padding: 5px !important;
  }
  .wraper {
    height: calc(50vh - 22px);
  }
  .slider,
  .right {
    width: 100%;
    height: calc(50vh - 22px);
  }
  h1 {
    font-size: 30px;
    padding: 20px 0 40px 0;
  }
  .slick-dots li button:before {
    font-size: 13px;
  }
  main {
    height: 100%;
  }
}
@media screen and (max-width: 480px) {
  h3 {
    font-size: 12px;
  }
  h2 {
    font-size: 17px;
    padding-bottom: 20px;
  }
  .wraper {
    height: 50vh;
  }
  .slick-dots {
    bottom: 15px;
  }
  .slider,
  .right {
    height: 100%;
  }
}
</style>
