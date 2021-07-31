<template>
  <div class="card">
		<p class="cardTitle">{{ info.title }}</p>
		<div class="cardContent">
			<p class="underLineText">{{	info.type }} | {{ info.group }} | {{ info.time }}</p>
			<p>{{ info.content }}</p>
			
		</div>
		<a-button type="primary" @click="clickUrl">
			<template #icon>
				<FolderOpenOutlined v-if="info.btnIcon === 'folder'"/>
				<ProjectOutlined v-else/>
			</template>
			{{ info.btnTitle }}
		</a-button>
		<a-divider />
	</div>
</template>
<script>
import { ProjectOutlined, FolderOpenOutlined } from '@ant-design/icons-vue';
export default {
	name: 'ProjectCard',
  props: ["info"],
  data() {
    return {
    };
  },
	components: {
    ProjectOutlined,
		FolderOpenOutlined
  },
  methods: {
    clickUrl() {
			window.open(this.info.btnUrl)
		}
  },
}
</script>
<style scoped>
@import url("./card.css");
.card {
	padding: 0;
}
.cardContent > p {
	margin-bottom: 3px;
}
.underLineText {
	text-decoration: underline;
}
.cardTitle, .cardContent  {
	margin-bottom: 10px;
}
</style>