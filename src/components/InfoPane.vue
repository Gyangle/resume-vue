<template>
  <div>
    <a-row style="height: auto">
      <a-col :span="12" class="introCol" style="background-color: #fff46d">
        <div class="intronBox">
          <div class="introBoxGreet">Hi! from Le(Grant) Yang</div>
          <div>
            Based at Las Vegas NV, I am a Software Engineer and Lacrosse Athlete
            from the University of Michigan School of Information. I'm
            interested in front-end, data visualization and recommendation
            system.
          </div>
        </div>
      </a-col>
      <a-col class="introCol" :span="12">
        <img src="../pic/personalPics/protrait.jpg" alt="a protrait of Grant" />
      </a-col>
    </a-row>
  </div>
  <div>
    <p class="introBoxGreet photoBoothText">Photobooth</p>
    <ant-carousel></ant-carousel>
  </div>
</template>

<script>
// const baseUrl = '../pic/personalPics/'
import AntCarousel from "./carousel/AntCarousel.vue"
export default {
  // setup() {
  //   const getImgUrl = i => {
  //     return `${baseUrl + i}.jpg`;
  //   };

  //   return {
  //     baseUrl,
  //     getImgUrl,
  //   };
  // },
  components: {
    AntCarousel,
  },
};
</script>

<style scoped>
img {
  width: auto;
  height: auto;
  max-width: 100%;
  max-height: 100%;
}
.intronBox {
  color: #3b117b;
  text-align: left;
  padding: 10% 20%;
}
.introCol {
  padding: auto;
  display: flex;
  align-items: center;
}
.introBoxGreet {
  margin-bottom: 20px;
  font-family: "Encode Sans", sans-serif;
  font-size: 40px;
  font-weight: bold;
}
.photoBoothText {
  color: #3b117b;
  text-align: left;
  padding: 20px 10%;
  margin-bottom: 0;
}
</style>