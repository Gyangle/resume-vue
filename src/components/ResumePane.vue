<template>
  <div class="personalInfo">
    <div class="personalName">Le Yang</div>
    <div>gyangle@umich.edu | 702-347-4943</div>
  </div>
  <div v-for="(card, index) in resumeCards" :key="index">
    <exp-card :info="card" />
  </div>
</template>

<script>
import ExpCard from "./card/ExpCard.vue";

export default {
  name: "resumePane",
  components: {
    ExpCard,
  },
  data() {
    const resumeCards = []
    return {
      resumeCards
    };
  },
  mounted() {
    fetch('http://localhost:5000/resume',{
      method:'GET',
		})
      .then(res => res.json())
      .then(data => this.resumeCards = data)
  }
};
</script>
<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
.personalInfo {
  color: #3b117b;
  padding: 25px 0;
  text-align: center;
  font-weight: bold;
  font-size: 18px;
}
.personalName {
  font-family: "Encode Sans", sans-serif;
  line-height: 1.41em;
  font-size: 40px;
}
</style>
