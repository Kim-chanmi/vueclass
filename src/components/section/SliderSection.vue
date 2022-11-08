<template>
  <section id="slider" class="slider__wrap nexon content__item">
    <h2 class="blind">슬라이드 영역</h2>
    <swiper
      :spaceBetween="30"
      :centeredSlides="true"
      :autoplay="{
        delay: 2500,
        disableOnInteraction: false,
      }"
      :pagination="{
        clickable: true,
      }"
      :navigation="true"
      :modules="modules"
      class="mySwiper"
    >
      <swiper-slide v-for="text in titles" v-bind:key="text.key">
        <div className="desc">
          <span>{{ text.span }}</span>
          <h3>{{ text.title }}</h3>
          <p>
            {{ text.desc }}
          </p>
          <div className="btn">
            <a href="/">{{ text.amore }}</a>
            <a href="/" className="black">{{ text.aview }}</a>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div className="desc" v-for="text in titles" v-bind:key="text.key">
          <span>{{ text.span }}</span>
          <h3>{{ text.title }}</h3>
          <p>
            {{ text.desc }}
          </p>
          <div className="btn">
            <a href="/">{{ text.amore }}</a>
            <a href="/" className="black">{{ text.aview }}</a>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div className="desc" v-for="text in titles" v-bind:key="text.key">
          <span>{{ text.span }}</span>
          <h3>{{ text.title }}</h3>
          <p>
            {{ text.desc }}
          </p>
          <div className="btn">
            <a href="/">{{ text.amore }}</a>
            <a href="/" className="black">{{ text.aview }}</a>
          </div>
        </div>
      </swiper-slide>
    </swiper>
  </section>
</template>
<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/pagination";
import "swiper/css/navigation";
import { Autoplay, Pagination, Navigation } from "swiper";

export default {
  data: function () {
    return {
      titles: [
        {
          span: "PLANT",
          title: "반려식물 키우기",
          desc: "반려식물 혼자 키우기 힘드시죠? \n우리가 당신과 함께하겠습니다.",
          amore: "자세히 보기",
          aview: "사이트 보기",
        },
      ],
    };
  },
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Autoplay, Pagination, Navigation],
    };
  },
};
</script>
<style>
.slider__inner {
  margin-top: 70px;
}

.slider {
  position: relative;
}

.slider__img {
  background: url(../../assets/img/slider_bg01.jpg) no-repeat center / cover;
  background: url(../../assets/img/slider_bg02.jpg) no-repeat center / cover;
  background: url(../../assets/img/slider_bg03.jpg) no-repeat center / cover;
}

.slider__img .desc {
  width: 1160px;
  margin: 0 auto;
  padding: 100px 20px;
}

.slider__img .desc span {
  font-size: 16px;
  background-color: #000;
  color: #fff;
  padding: 1px 14px 0 14px;
  border-radius: 30px;
  text-transform: uppercase;
  margin-bottom: 10px;
  display: inline-block;
}

.slider__img .desc h3 {
  font-size: 110px;
  font-weight: 300;
  line-height: 1;
  text-transform: uppercase;
  margin-bottom: 16px;
  margin-left: -8px;
}

.slider__img .desc p {
  font-size: 20px;
  font-weight: 300;
  line-height: 1.35;
  margin-bottom: 130px;
}

.slider__img .desc .btn a {
  font-size: 16px;
  background-color: rgb(115, 115, 115);
  color: #fff;
  padding: 11px 50px;
  display: inline-block;
}

.slider__img .desc .btn a.black {
  background: #000;
  color: #fff;
}

.slider__arrow a {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  width: 30px;
  height: 56px;
  background-image: url(../../assets/img/slider_icon.svg);
}

.slider__arrow a.left {
  left: 20px;
}

.slider__arrow a.right {
  right: 20px;
  background-position: -50px 0;
}

.slider__dot {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  bottom: 25px;
}

.slider__dot a {
  display: inline-block;
  width: 16px;
  height: 16px;
  background-image: url(../../assets/img/slider_icon.svg);
  background-position: -20px -70px;
}

.slider__dot a.active {
  background-position: 0px -70px;
}

.slider__dot a.play {
  background-position: -40px -70px;
}

.slider__dot a.stop {
  background-position: -60px -70px;
}

/* swiper */
.swiper-slide:nth-child(1) {
  background: url(../../assets/img/slider_bg01.jpg) no-repeat center / cover;
}

.swiper-slide:nth-child(2) {
  background: url(../../assets/img/slider_bg02.jpg) no-repeat center/ cover;
}

.swiper-slide:nth-child(3) {
  background: url(../../assets/img/slider_bg03.jpg) no-repeat center/ cover;
}

.swiper-slide .desc {
  width: 1160px;
  margin: 0 auto;
  padding: 100px 20px;
  box-sizing: border-box;
}

.swiper-slide .desc span {
  font-size: 16px;
  background-color: #000;
  color: #fff;
  padding: 1px 14px 0 14px;
  border-radius: 30px;
  text-transform: uppercase;
  margin-bottom: 10px;
  display: inline-block;
}

.swiper-slide .desc h3 {
  font-size: 110px;
  font-weight: 300;
  line-height: 1;
  text-transform: uppercase;
  margin-bottom: 16px;
  margin-left: -8px;
}

.swiper-slide .desc p {
  font-size: 20px;
  font-weight: 300;
  line-height: 1.35;
  margin-bottom: 130px;
  white-space: pre-wrap;
}

.swiper-slide .desc .btn a {
  font-size: 16px;
  background-color: rgb(115, 115, 115);
  color: #fff;
  padding: 11px 50px;
  display: inline-block;
}

.swiper-slide .desc .btn a.black {
  background: #000;
  color: #fff;
}

.swiper-button-next,
.swiper-button-prev {
  width: 30px !important;
  height: 56px !important;
  background: url(../../assets/img/slider_icon.svg);
}

.swiper-button-next {
  background-position: -50px 0;
}

.swiper-button-next:after,
.swiper-button-prev:after {
  opacity: 0;
}

.swiper-pagination-bullet {
  width: 16px !important;
  height: 16px !important;
  background-image: url(../../assets/img/slider_icon.svg) !important;
  background-position: -20px -70px !important;
  background-color: transparent !important;
  opacity: 1 !important;
}

.swiper-pagination-bullet-active {
  background-position: 0px -70px !important;
}

.swiper-button {
  display: flex;
  position: absolute;
  left: 50%;
  margin-left: 40px;
  bottom: 24px;
  z-index: 1000;
}

.swiper-button-stop {
  background-image: url(../../assets/img/slider_icon.svg);
  background-position: -60px -70px;
  width: 16px;
  height: 16px;
  cursor: pointer;
}

.swiper-button-play {
  background-image: url(../../assets/img/slider_icon.svg);
  background-position: -40px -70px;
  width: 16px;
  height: 16px;
  cursor: pointer;
}

/* media */
@media (max-width: 960px) {
  .swiper-slide .desc {
    width: 100%;
    text-align: center;
  }

  .swiper-slide .desc h3 {
    font-size: 70px;
  }
}

@media (max-width: 600px) {
  .swiper-slide .desc {
    padding: 80px 0;
  }

  .swiper-slide .desc h3 {
    font-size: 40px;
  }

  .swiper-slide .desc p {
    font-size: 16px;
    margin-bottom: 50px;
  }

  .swiper-slide .desc .btn a {
    padding: 10px 25px;
  }
}
</style>
