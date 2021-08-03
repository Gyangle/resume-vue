<template>
  <div v-for="(card, index) in projectCards" :key="index">
    <project-card :info="card"></project-card>
  </div>
  
</template>

<script>
import ProjectCard from './card/ProjectCard.vue'
export default {
  name: "ProjectPane",
  components: {
    ProjectCard,
  },
  data() {
    let projectCards = []
    return {
      projectCards
    };
  },
  mounted() {
    fetch('http://localhost:5000/project',{
      method:'GET',
		})
      .then(res => res.json())
      .then(data => this.projectCards = data)
  },
  methods: {
    handleClick() {
      console.log(this.content);
    },
  },
};
</script>

<style scoped>

</style>