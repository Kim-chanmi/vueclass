<template>
  <section id="imageType" class="image__wrap content__item" :class="attr">
    <h2>반려식물 키우기</h2>
    <p>반려식물을 기르는 분들을 위한 사이트 입니다.</p>
    <div class="image__inner" :class="layout">
      <article class="image img1">
        <h3 class="image__title">식물의 종류</h3>
        <p class="image__desc">
          다양한 식물의 종류들을 알아볼 것입니다. 초보자가 기르기 쉬운 식물,
          공기정화에 탁월한 식물, 선물하기 좋은 식물 등을 알아볼 예...
        </p>
        <a class="image__btn" href="#" title="자세히 보기">자세히보기</a>
      </article>
      <article class="image img2">
        <h3 class="image__title">인테리어</h3>
        <p class="image__desc">
          식물을 이용한 다양한 인테리어들을 알아볼 것입니다. 식물의 크기에 따른
          공간, 위치 등등이 있습니다. 많은 예시들이 있으니 구경...
        </p>
        <a class="image__btn yellow" href="#" title="자세히 보기">자세히보기</a>
      </article>
    </div>
  </section>
</template>
<script>
export default {
  props: {
    attr: String,
    layout: String,
  },
};
</script>
<style>
.image__inner {
  display: flex;
  justify-content: space-between;
}
.image {
  width: 49%;
  height: 370px;
  padding: 200px 30px 30px 30px;
  box-sizing: border-box;
}
.image.img1 {
  background: url(../../assets/img/img_bg_01.jpg) no-repeat center / cover;
}
.image.img2 {
  background: url(../../assets/img/img_bg_02.jpg) no-repeat center / cover;
}
.image__title {
  font-size: 32px;
  margin-bottom: 10px;
  color: #000;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.image__desc {
  font-size: 18px;
  margin-bottom: 10px;
  line-height: 1.4;
  font-weight: 300;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
}
.image.img1 .image__desc {
  color: #000;
}
.image.img2 .image__desc {
  color: #fff;
}
.image__btn {
  padding: 10px 20px;
  background-color: #da7740;
  font-size: 16px;
  color: #fff;
  text-align: center;
  font-weight: 300;
  display: inline-block;
}
.image__btn.yellow {
  background-color: #daad40;
}
@media (max-width: 960px) {
}
@media (max-width: 600px) {
  .image__inner {
    flex-direction: column;
  }
  .image {
    width: 100%;
    padding: 210px 20px 20px 20px;
  }
  .image:first-child {
    margin-bottom: 20px;
  }
  .image__title {
    font-size: 24px;
  }
}
</style>
