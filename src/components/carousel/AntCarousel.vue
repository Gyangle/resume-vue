<template>
  <div class="container">
    <a-carousel autoplay arrows>
      <template #prevArrow>
      <div class="custom-slick-arrow" style="left: 10px; z-index: 1">
        <LeftOutlined/>
      </div>
    </template>
    <template #nextArrow>
      <div class="custom-slick-arrow" style="right: 10px">
        <RightOutlined/>
      </div>
    </template>
      <div>
        <img
          src="../../pic/personalPics/4.jpg"
          alt="tibet decloration"
        />
      </div>
      <div>
        <img
          src="../../pic/personalPics/2.jpg"
          alt="national team"
        />
      </div>
      <div>
        <img
          src="../../pic/personalPics/3.jpg"
          alt="light house"
        />
      </div>
      <div>
        <img
          src="../../pic/personalPics/1.jpg"
          alt="concrete canoe"
        />
      </div>
    </a-carousel>
  </div>
</template>
<script>
import { LeftOutlined, RightOutlined  } from '@ant-design/icons-vue'
export default ({
  components: {
    LeftOutlined,
    RightOutlined ,
  },
});
</script>
<style scoped>
.ant-carousel :deep(.slick-slide) {
  text-align: center;
  height: auto;

  /* controls how tall is the slider */
  /* line-height: -160px; */

  background: inherit;
  overflow: visible;
}

.ant-carousel :deep(.slick-arrow.custom-slick-arrow) {
  width: 60px;
  height: 60px;
  font-size: 60px;
  color: #fff;
  background-color: inherit;
  opacity: 0.7;
}
.ant-carousel :deep(.slick-slide img) {
  display: block;
  margin: auto;
  max-width: 100%;
  height: auto;
}
.ant-carousel :deep(.custom-slick-arrow:before) {
  display: none;
}
.ant-carousel :deep(.custom-slick-arrow:hover) {
  opacity: 0.9;
}
.container {
  max-width: 700px;
  height: auto;
  margin: auto;
}
</style>