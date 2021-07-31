<template>
  <div v-for="(card, index) in allCards" :key="index">
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
    let allCards = [
      {
      title: 'Digital Humanities: Diary Viewer from Svoboda Diary Project',
      type: 'Direct Research Group',
      group: 'Near Eastern Languages & Civilization Department',
      time: 'April 2020 – Now',
      content: 'Updated the user interface of the key feature of the project’s website, the “Diary Viewer”, and publish the new diaries for "Diary Viewer" to use. Created a new production pipeline to incorporate the templates/themes.',
      btnTitle: 'Project Page',
      btnUrl: 'https://devpost.com/software/easy-learn',
      btnIcon: 'folder' // 'folder' when the icon is a folder
    },
    {
      title: 'Digital Humanities: Diary Viewer from Svoboda Diary Project',
      type: 'Direct Research Group',
      group: 'Near Eastern Languages & Civilization Department',
      time: 'April 2020 – Now',
      content: 'Updated the user interface of the key feature of the project’s website, the “Diary Viewer”, and publish the new diaries for "Diary Viewer" to use. Created a new production pipeline to incorporate the templates/themes.',
      btnTitle: 'Project Page',
      btnUrl: 'https://devpost.com/software/easy-learn',
      btnIcon: '' // 'folder' when the icon is a folder
    },
    {
      title: 'Digital Humanities: Diary Viewer from Svoboda Diary Project',
      type: 'Direct Research Group',
      group: 'Near Eastern Languages & Civilization Department',
      time: 'April 2020 – Now',
      content: 'Updated the user interface of the key feature of the project’s website, the “Diary Viewer”, and publish the new diaries for "Diary Viewer" to use. Created a new production pipeline to incorporate the templates/themes.',
      btnTitle: 'Project Page',
      btnUrl: 'https://devpost.com/software/easy-learn',
      btnIcon: '' // 'folder' when the icon is a folder
    }
    ]
    return {
      // card,
      allCards
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

</style>