<template>
  <div class="hello">
    hellohello
  </div>
  <exp-card :info="singleCard" />
</template>

<script>
import ExpCard from './card/ExpCard.vue'

export default {
  name: 'resumePane',
  components: {
    ExpCard
  },
  props: {
  },
  data() {
    const singleCard = {
      position: 'Front-end Intern',
      time: 'April 2020 - Now', group: 'UW Near Eastern Languages & Civilization Department',
      content: ['First line First line First line First line First line ',
                'Second line Second lineSecond Second lineSecond lineSecond line',
                'third line third line third line third line third line third line']
    }
    return {
      singleCard
    }
  },
  methods: {
  }
}
</script>
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
