<template>
  <v-app data-scroll-container>
    <div class="hero d-flex align-center justify-center">
      <div class="text-center">
        <p
          data-scroll
          data-scroll-speed="1"
          class="text-h3 text-yellow animate__animated animate__fadeInDown"
        >
          مكتب الضوء <span class="white--text">الابيض</span> للخادمات
        </p>
        <v-btn
          data-scroll
          data-scroll-speed="1"
          text
          color="#eeb328"
          x-large
          class="
            text-h6
            animate__animated animate__fadeInDown animate__delay-1s
          "
          @click="locoScroll.scrollTo('#contact')"
          ><v-icon size="29" class="mx-2">mdi-phone</v-icon>تواصل معنا
          الان</v-btn
        >
      </div>
    </div>
    <v-container>
      <v-row>
        <v-col cols="12">
          <v-img
            eager
            data-scroll
            data-scroll-speed="1"
            :src="require('~/assets/macbook.png')"
            contain
            class="align-center text-center mx-auto justify-center"
            height="100%"
            width="100%"
          >
            <div>
              <span
                data-scroll
                data-scroll-speed="1"
                class="
                  text-center
                  white--text
                  macbookText
                  text-h5
                  d-inline-block
                "
                style="width: 50%"
                :class="[
                  $vuetify.breakpoint.mdAndUp ? 'text-h5' : 'text-body-1',
                ]"
              >
                مطلوب خادمات من جميع الجنسيات باسرع وقت لانجاز المعاملة
              </span>
              <br />
              <br />
              <v-btn
                data-scroll
                data-scroll-speed="1"
                text
                color="#eeb328"
                large
                class="text-h5"
                :class="[
                  $vuetify.breakpoint.mdAndUp ? 'text-h5' : 'text-body-1',
                ]"
                @click="locoScroll.scrollTo('#contact')"
                ><v-icon size="20" class="mx-2">mdi-phone</v-icon>تواصل معنا
                الان</v-btn
              >
            </div>
          </v-img>
        </v-col>
      </v-row>
    </v-container>
    <div class="features white--text pa-10">
      <p data-scroll data-scroll-speed="1" class="text-center text-h5">
        المميزات
      </p>
      <ul
        data-scroll
        data-scroll-speed="1"
        class="text-h6 mr-md-12"
        style="direction: rtl"
      >
        <li>نأسف لعدم وجود شغالات إيجار</li>
        <li>هل لديكم عاملات مربيات ممرضات طباخات</li>
        <li>شغالات رافضات العمل وتريدون التنازل عنهم بأسرع وقت وبدون خساره</li>
        <li>يوجد لدينا مترجمين لسهوله اقناعهم من جميع الجنسيـات</li>
        <li>قسم خاص لاستلام ورعاية الخدم</li>
        <li>
          لدينا عدد كبير من العملاء يثقون فى مكتبنا ويرغبون فى خادمات للتنازل
        </li>
        <li>نحن نقوم بجميع الأجراءات القانونيه</li>
        <li>( نقل الكفاله ـ اصدار الاقامه ـ دفع الغرامه ـ وغيره)</li>
        <li>عقود رسمية لضمان حقوق جميع الاطراف</li>
        <li>باعلي الاسعار تعوضك خسارة الاستقدام</li>
        <li>نقل الكفالة فى مدة وجيزة</li>
      </ul>
      <div class="swiper-3d">
        <swiper
          data-scroll
          data-scroll-speed="1"
          class="swiper"
          :options="swiperOption_3d"
        >
          <swiper-slide
            v-for="(img, index) in imgs"
            :key="index"
            style="width: 300px; height: 300px"
            ><v-img eager width="100%" height="100%" :src="img"> </v-img
          ></swiper-slide>

          <div slot="pagination" class="swiper-pagination"></div>
          <div
            slot="button-prev"
            class="swiper-button-prev"
            style="color: #eeb328"
          ></div>
          <div
            slot="button-next"
            class="swiper-button-next"
            style="color: #eeb328"
          ></div>
        </swiper>
      </div>
    </div>

    <div class="pa-10">
      <p
        id="contact"
        data-scroll
        data-scroll-speed="1"
        class="text-center text-h5"
      >
        تواصل معنا عن طريق واتس اب
        <v-icon size="30" color="#03E776">mdi-whatsapp</v-icon>
      </p>
      <v-row>
        <v-col
          v-for="(item, index) in whats"
          :key="index"
          cols="12"
          md="3"
          data-scroll
          data-scroll-speed="1"
        >
          <v-card
            :href="`https://api.whatsapp.com/send?phone=+966${item}`"
            target="_blank"
            max-height="60"
          >
            <v-img
              max-height="60"
              eager
              class="white--text align-end"
              :src="
                require('~/assets/mika-baumeister-uKdkh25_wc0-unsplash.jpeg')
              "
              gradient="#000000a0,#00000090"
            >
              <v-card-title class="justify-center"> 0{{ item }} </v-card-title>
            </v-img>
          </v-card>
        </v-col>
      </v-row>
    </div>
    <v-divider></v-divider>
    <div class="pa-10">
      <p data-scroll data-scroll-speed="1" class="text-center text-h5">
        تواصل معنا عن طريق الجوال
        <v-icon size="30" color="black">mdi-cellphone</v-icon>
      </p>
      <v-row>
        <v-col
          v-for="(item, index) in mobiles"
          :key="index"
          cols="12"
          md="3"
          data-scroll
          data-scroll-speed="1"
        >
          <v-card :href="`tel:+966${item}`" target="_blank" max-height="60">
            <v-img
              max-height="60"
              eager
              class="white--text align-end"
              :src="require('~/assets/freestocks-GxM9gkLJbwY-unsplash.jpeg')"
              gradient="#000000a0,#00000090"
            >
              <v-card-title class="justify-center">0{{ item }}</v-card-title>
            </v-img>
          </v-card>
        </v-col>
      </v-row>
    </div>
  </v-app>
</template>

<script>
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'
export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      locoScroll: null,
      swiperOption: {
        slidesPerView: 3,
        spaceBetween: 30,
        pagination: {
          el: '.swiper-pagination',
          clickable: true,
        },
        breakpoints: {
          768: {
            slidesPerView: 3,
            spaceBetween: 30,
          },
          640: {
            slidesPerView: 2,
            spaceBetween: 20,
          },
          320: {
            slidesPerView: 1,
            spaceBetween: 10,
          },
        },
      },
      swiperOption_3d: {
        effect: 'coverflow',
        grabCursor: true,
        centeredSlides: true,
        slidesPerView: 'auto',
        autoplay: {
          delay: 2500,
          disableOnInteraction: false,
        },
        coverflowEffect: {
          rotate: 50,
          stretch: 0,
          depth: 100,
          modifier: 1,
          slideShadows: true,
        },
        pagination: {
          el: '.swiper-pagination',
        },
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev',
        },
      },
      imgs: [
        '/logo.png',
        require('~/assets/pexels-monstera-5996954.jpeg'),
        require('~/assets/pexels-anete-lusina-6331144.jpeg'),
        require('~/assets/pexels-cottonbro-6466228.jpeg'),
        require('~/assets/pexels-cottonbro-6466482.jpeg'),
        '/logo.png',
        require('~/assets/pexels-polina-tankilevitch-4440568.jpeg'),
        require('~/assets/pexels-rodnae-productions-5591859.jpeg'),
        require('~/assets/pexels-karolina-grabowska-4239103.jpeg'),
        require('~/assets/pexels-monstera-5331123.jpeg'),
        '/logo.png',
      ],
      whats: ['555966245', '555366343', '555148665', '555416673'],
      mobiles: ['555148665', '555366343', '555966245', '555416673'],
    }
  },

  mounted() {
    /* eslint-disable-next-line */
    const locomotiveScroll = new this.locomotiveScroll({
      el: document.querySelector('[data-scroll-container]'),
      smooth: true,

      tablet: {
        smooth: true,
      },
      smartphone: {
        smooth: true,
      },
    })
    this.locoScroll = locomotiveScroll

    setTimeout(() => {
      locomotiveScroll.update()
    }, 5000)
  },
}
</script>

<style>
.hero {
  height: 100vh;
  width: 100vw;
  background-image: linear-gradient(#000000a0, #000000a0),
    url('~assets/clayton-1by_GbwEMwc-unsplash.jpeg');
  background-size: cover;
  background-position: center;
}
.text-yellow {
  color: #eeb328;
}
.macbookText {
  text-shadow: 0 0.5px 15px #fff;
}
.features {
  background-image: linear-gradient(#000000b0, #000000b0),
    url('~assets/watermark-designs-XL6gfkLmkOw-unsplash.jpeg');
  background-size: cover;
  background-position: center;
}
.swiper-3d {
  width: 100%;
  height: 400px;
  padding-top: 50px;
  padding-bottom: 50px;
}

.swiper
  .swiper-pagination
  .swiper-pagination-bullet.swiper-pagination-bullet-active {
  background-color: #eeb328;
}
</style>
