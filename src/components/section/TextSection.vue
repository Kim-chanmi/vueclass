<template>
  <section id="textType01" class="text__wrap content__item" :class="attr">
    <span>다양한 꿀Tip!</span>
    <h2 class="mb70">반려식물 기르기</h2>
    <div class="text__inner" :class="layout">
      <div
        class="text"
        :class="text.class"
        v-for="text in titles"
        v-bind:key="text.key"
      >
        <h3 class="text__title">{{ text.title }}</h3>
        <p class="text__desc">
          {{ text.desc }}
        </p>
        <a class="text_btn" href="/">{{ text.amore }}</a>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  props: {
    attr: String,
    layout: String,
  },

  data: function () {
    return {
      top: {
        span: "다양한 꿀Tip!",
        title: "반려식물 기르기",
      },
      titles: [
        {
          title: "분갈이",
          desc: "분갈이 시기와 정확한 방법을 알고 계신가요? 식물에 맞는 화분도 따로 있답니다. 여기서는 분갈이 시기와 정확한 방법을 알...",
          class: "t1",
          amore: "더보기",
        },
        {
          title: "물 주기",
          desc: "식물마다 얼마나 자주, 어느 정도의 물을 줘야 하는지 궁금하시죠? 식물에게 물을 주는 정확한 방법을 알려드리겠습니다.",
          class: "t2",
          amore: "더보기",
        },
        {
          title: "인테리어",
          desc: "식물을 이용한 다양한 인테리어들이 있습니다. 집의 구조와 환경에 맞는 다양한 인테리어들을 볼 수 있습니다.",
          class: "t3",
          amore: "더보기",
        },
        {
          title: "영양분",
          desc: "사람이 영양제를 섭취하듯이 식물들도 영양분이 필요합니다. 식물마다 필요한 영양분에 대해 알아보겠습니다.",
          class: "t4",
          amore: "더보기",
        },
        {
          title: "병충해",
          desc: "식물을 키우면 벌레가 생길까봐, 그리고 그 벌레로 인해 식물이 죽을까봐 걱정이 많으시죠? 그 예방법에 대해 알아보겠습니다.",
          class: "t5",
          amore: "더보기",
        },
        {
          title: "계절관리",
          desc: "계절의 변화에 따라 온도와 습도가 달라지게 됩니다. 이러한 환경에 식물들은 큰 영향을 받는데요. 계절 변화에 따른 관리법을...",
          class: "t6",
          amore: "더보기",
        },
      ],
    };
  },
};
</script>
<style>
/* textType */
.text__inner {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
.text {
  width: 32%;
  margin-bottom: 2%;
  padding: 20px;
  box-sizing: border-box;
  border-radius: 10px;
  transition: background 0.4s;
}
.text:hover {
  background: #f5f5f5;
}
.text__title {
  font-size: 24px;
  line-height: 1;
  margin-bottom: 10px;
  word-spacing: nowrap;
  text-overflow: ellipsis;
  position: relative;
  padding-top: 75px;
}
.text__title::before {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  width: 60px;
  height: 60px;
  background: url(../../assets/img/text_icon.svg);
}
.text.t1 .text__title::before {
  background-position: 0 0;
}
.text.t2 .text__title::before {
  background-position: -60 0;
}
.text.t3 .text__title::before {
  background-position: -120 0;
}
.text.t4 .text__title::before {
  background-position: -180 0;
}
.text.t5 .text__title::before {
  background-position: -240 0;
}
.text.t6 .text__title::before {
  background-position: -300 0;
}
.text__desc {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.4;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  color: #666;
  margin-bottom: 20px;
}
.text_btn {
  font-size: 16px;
  line-height: 1;
  text-decoration: underline;
  text-underline-position: under;
  color: #666;
}
@media (max-width: 960px) {
  .text {
    width: 49%;
    background: #f5f5f5;
  }
}
@media (max-width: 600px) {
  .text__title {
    font-size: 20px;
  }
  .text__desc {
    font-size: 16px;
  }
}
@media (max-width: 480px) {
  .text {
    width: 100%;
  }
}
</style>
