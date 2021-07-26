<template>
  <div class="personalInfo">
    <div class="personalName">Le Yang</div>
    <div>gyangle@umich.edu | 702-347-4943</div>
  </div>
  <div v-for="(card, index) in allCards" :key="index">
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
  props: {},
  data() {
    const singleCard = {
      position: "Front-end Intern",
      time: "April 2020 - Now",
      group: "UW Near Eastern Languages & Civilization Department",
      content: [
        "First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line ",
        "Second line Second lineSecond Second lineSecond lineSecond line",
        "third line third line third line third line third line third line",
      ],
    };
    const allCards = [
      {
        position: "Front-end Intern",
        time: "April 2020 - Now",
        group: "UW Near Eastern Languages & Civilization Department",
        content: [
          "First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line ",
          "Second line Second lineSecond Second lineSecond lineSecond line",
          "third line third line third line third line third line third line",
        ],
      },
      {
        position: "Front-end Intern",
        time: "April 2020 - Now",
        group: "UW Near Eastern Languages & Civilization Department",
        content: [
          "First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line ",
          "Second line Second lineSecond Second lineSecond lineSecond line",
          "third line third line third line third line third line third line",
        ],
      },
      {
        position: "Front-end Intern",
        time: "April 2020 - Now",
        group: "UW Near Eastern Languages & Civilization Department",
        content: [
          "First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line First line ",
          "Second line Second lineSecond Second lineSecond lineSecond line",
          "third line third line third line third line third line third line",
        ],
      },
    ];
    return {
      singleCard,
      allCards, // all cards in an array
    };
  },
  methods: {},
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
