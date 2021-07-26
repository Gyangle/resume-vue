<template>
  <a-row class="card" :gutter="30">
    <a-col :span="6">
      <div class="cardPosition">
        {{ info.position }}
      </div>
      <div class="cardTime">
        {{ info.time }}
      </div>
    </a-col>
    <a-col :span="18">
      <div>
        <div class="cardGroup">
          {{ info.group }}
        </div>
        <div class="cardContent">
          <ul>
            <li v-for="(exp, index) in content" :key="index">
              {{ exp }}
            </li>
          </ul>
        </div>
      </div>
    </a-col>
  </a-row>
</template>
<script>
export default {
  name: "ExpCard",
  props: ["info"],
  data() {
    let content = this.info.content;
    return {
      content, // description of the content, in array
    };
  },
  methods: {
    handleClick() {
      console.log(this.content);
    },
  },
};
</script>
<style scoped>
.card {
  color: #3b117b;
  padding: 25px 0;
	margin: auto !important;
	width: 60%;
  text-align: left;
}
.cardPosition {
  font-family: "Encode Sans", sans-serif;
  line-height: 1.41em;
  font-size: 22px;
  font-weight: bold;
}
.cardTime {
  font-size: 15px;
}
.cardGroup {
  font-family: "Encode Sans", sans-serif;
  font-size: 18px;
  font-weight: bold;
}
.cardContent {
  line-height: 1.875em;
  font-size: 15px;
}
.cardContent > ul {
	padding-left: 30px;
}
</style>