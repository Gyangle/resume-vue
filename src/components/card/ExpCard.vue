<template>
		<a-row class="card">
			<a-col :span="8">
				<div class="position">
					{{info.position}}
				</div>
				<div class="time">
					{{info.time}}
				</div>
			</a-col>
			<a-col :span="16">
				<div >
					<div class="group">
						{{info.group}}
					</div>
					<div class="content">
						<ul>
							<li v-for="(exp, index) in content" :key="index">
								{{exp}}
							</li>
						</ul>
					</div>
				</div>
			</a-col>
		</a-row>
</template>
<script>
export default {
    name: 'ExpCard',
    props: ['info'],
		data() {
			let content = this.info.content
			return {
				content // description of the content, in array
			}
		},
    methods: {
    handleClick() {
      console.log(this.content)
    }
  }
}
</script>
<style scoped>
    .card {
			color: #3b117b;
			padding: 50px 200px;
			text-align: left;
		}
		.position {
			line-height:1.41em;
			font-size:22px;
			font-weight: bold;
		}
		.time {
			font-size:15px
		}
		.group {
			font-size:18px;
			font-weight: bold;
		}
		.content {
			line-height:1.875em;
			font-size:15px
		}
</style>