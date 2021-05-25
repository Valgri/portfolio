<template>
  <div class="right">
    <h1>Portfolio of my works</h1>
    <VueSlickCarousel ref="c2" v-bind="settings">
      <section class="wrapper" v-for="(ab, i) in about" :key="i">
        <h2>{{ ab.title }}</h2>
        <p>{{ ab.text }}</p>
        <a :href="ab.href" v-if="ab.href != null" target="_blank" rel="noopener"
          >Link for site</a
        >
<!--        <a :href="ab.git" v-if="ab.git != null" target="_blank" rel="noopener"-->
<!--          >Link for github</a-->
<!--        >-->
      </section>
      <template #prevArrow="arrowOption">
        <div class="custom-arrow">
          {{ arrowOption.currentSlide }}
        </div>
      </template>
      <template #nextArrow="arrowOption">
        <div class="custom-arrow">
          {{ arrowOption.currentSlide }}
        </div>
      </template>
    </VueSlickCarousel>
  </div>
</template>

<script>
import VueSlickCarousel from "vue-slick-carousel";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
// optional style for arrows & dots
import "vue-slick-carousel/dist/vue-slick-carousel-theme.css";

export default {
  name: "Rightbar",
  components: { VueSlickCarousel },
  data() {
    return {
      about: [
        {
          title: "Villageatrancharrah",
          text:
            "Создание Landing page с интеграцией Google Map, валидация форм, отправка заявки с использованием php скрипта и mailchimp. В последствии переделанный под полноценный блог.",
          href: "https://villageatrancharrah.com/",
        },
        {
          title: "Statewatch",
          text:
            "Натяжка готовой вёрстки на cms Wordpress (использование плагинов ACF, CF7, CPT, создание фильтров, работа с customizer)",
          href: "https://statewatch.org.ua/",
        },
        {
          title: "Peaceful",
          text:
            "Front-end разработка сайта по готовому дизайну с нуля, написание кастомных скриптов,анимаций. Верстка под Woocommerce, Pixel-perfect.",
          href: "https://peacefulsquirrelbox.com/",
        },
        {
          title: "Агрокультура",
          text:
            "Front-end разработка сайта по готовому дизайну с нуля, натяжка на cms Wordpress (использование плагинов ACF, CF7, CPT, создание фильтров, работа с customizer, maskedinput)",
          href: "https://agrocultura.ru/",
        },
        {
          title: "Monamor",
          text:
            "Front-end разработка сайта по готовому дизайну с нуля, написание кастомных скриптов, анимаций. Верстка под Woocommerce, Pixel-perfect.",
          href: "https://monamor.latrunculorum.com",
        },
        {
          title: "Flornoy",
          text:
            "Pixel-perfect Front-end разработка сайта по готовому дизайну с нуля, написание кастомных скриптов, анимаций. Pixel-perfect вёрстка.",
          href: "https://www.flornoy.com/",
        },
        {
          title: "Bloggers.social-star",
          text:
            "Front-end разработка сайта по готовому дизайну с нуля, написание кастомных скриптов, анимаций. Натяжка готовой вёрстки на cms Wordpress",
          href: "https://bloggers.social-stars.ru/",
        },
        {
          title: "Youtuber.social-star",
          text:
            "Front-end разработка сайта по готовому дизайну с нуля, написание кастомных скриптов, анимаций.",
          href: "https://youtube.social-stars.ru/",
        },
        {
          title: "Yavsotne",
          text:
            "Натяжка готовой вёрстки на cms Wordpress. (использование плагинов ACF, CF7, создание счётчика просмотров с помощью СRON.)  ",
          href: "https://yavsotne.ru/",
        },
        {
          title: "Viv-home",
          text:
            "Front-end разработка страницы для сайта по готовому дизайну, написание скрипта для отображения счетчика подсчета отзывов.",
          href: "https://www.viv-home.fr/avis-des-clients-vivhome/",
        },
        {
          title: "Vue crm",
          text:
            "Проект для самостоятельно обучения Vue, Vuex, Vue router, аутентификации, создание Vue фильтров, работа с Api по конвертации валют, подключение firebase. ",
          href: "https://vue-crm-df4f9.web.app/login?message=login",
          git: "https://github.com/Valgri/Vue-crm",
        },
        {
          title: "Online-shop ( Node.js(Express) + MongoDB )",
          text:
            "Проект для самостоятельно обучения Node.js (Express), MongoDB.",
          git: " https://github.com/Valgri/Online-shop",
        },
        {
          title: "React quiz (pet project)",
          text:
            "Проект для самостоятельно обучения React, Redux, React router, подключение firebase.",
          href: "https://react-quiz-a3b5f.web.app/",
        },
        {
          title: "Fullstack Rest api ",
          text:
            "Проект для самостоятельно обучения работы Rest api. Используется Vue + Node(Express). Взаимодействия сервера с клиентом.",
          git: "https://github.com/Valgri/Fullstack-Rest-api-",
        },
        {
          title: "Anagog",
          text:
            "Front-end разработка новых страниц сайта, обновление дизайна, bugfix.",
          href: "https://www.anagog.com/",
        },
        {
          title: "MERN app",
          text: `Учебное приложение с использование MERN стека.
                        Реализована защита роутов, авторизация, возможность добавить ссылку для её сокращения, редирект по клику на сокращенную ссылку, подсчёт кликов.
                        На backend задействованы - JWT, Bcrypt. Для авторизации и шифрования паролей.
                        На клиенте используются собственные хуки аутентификации, сообщений, и роутов.`,
          git: "https://github.com/Valgri/mern_app",
        },
        {
          title: "vti.km.ua",
          text: `Front-end разработка сайта по готовому дизайну с нуля, написание кастомных скриптов, работа с canvas. Использование css/js анимаций. Оптимизация сайта по сервису lighthouse.`,
          href: "https://vti.km.ua/",
        },
      ],

      settings: {
        slidesToShow: 1,
        arrows: true,
        focusOnSelect: true,
        asNavFor: this.$parent.$children[0].$refs.c1,
        fade: true,
      },
    };
  },
};
</script>

<style lang="scss" scoped>
.slick-slider {
  max-width: 90%;
}
.wrapper {
  padding-bottom: 10px;
}
a {
  padding-top: 80px;
  display: block;
  text-decoration: none;
  color: #bf4442;
  font-weight: 400;
  cursor: pointer;
  position: relative;
  max-width: max-content;
}
a:before {
  content: "";
  position: absolute;
  left: 0;
  bottom: -5px;
  width: 0;
  height: 3px;
  background-color: #837888;
  transition: 0.3s linear;
}
a:last-child {
  padding-top: 20px;
}
a:hover {
  color: #837888;
}
a:hover:before {
  right: 0;
  width: 100%;
}
p {
  line-height: 1.6;
}
.custom-arrow.slick-prev:before {
  transform: rotate(180deg);
}
.custom-arrow.slick-next:before,
.custom-arrow.slick-prev:before {
  content: "";
  background: url("../assets/Arrow.af06d28e.svg");
  width: 20px;
  height: 20px;
  position: absolute;
  background-repeat: no-repeat;
  background-position: 100%;
}
@media screen and (max-width: 1024px) {
  a {
    padding-top: 30px;
  }
}
</style>

