<template>
  <div id="components-layout-demo-basic">
      <a-layout>
        <a-layout-header>My SIte</a-layout-header>
        <a-layout-content>
          <a-tabs type="line" defaultActiveKey="2">
            <a-tab-pane key="1" tab="RESUME">
              <ResumePane/>
            </a-tab-pane>
            <a-tab-pane key="2" tab="ABOUT">
              <InfoPane/>
            </a-tab-pane>
            <a-tab-pane key="3" tab="PROJECT&WORK">
              <ProjectPane/>
            </a-tab-pane>
          </a-tabs>
        </a-layout-content>
        <a-layout-footer>Footer</a-layout-footer>
      </a-layout>
  </div>

</template>

<script>
import ResumePane from './components/ResumePane.vue'
import InfoPane from './components/InfoPane.vue'
import ProjectPane from './components/ProjectPane.vue'
export default {
  name: 'App',
  components: {
    ResumePane,
    InfoPane,
    ProjectPane,
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Encode+Sans:wght@700&family=Open+Sans&display=swap');
#app {
  font-family: 'Open Sans', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #3b117b;
}
#components-layout-demo-basic .ant-layout-header,
#components-layout-demo-basic .ant-layout-footer {
  background: #443c3c60;
  color: rgba(255, 255, 255, 0.933);
}
#components-layout-demo-basic .ant-layout-footer {
  line-height: 1.5;
}
#components-layout-demo-basic .ant-layout-sider {
  background: #4f4f50;
  line-height: 120px;
}
#components-layout-demo-basic .ant-layout-content {
  background: #dad7df;
  min-height: 120px;
  line-height: 120px;
  margin: auto;
}
#components-layout-demo-basic > .ant-layout {
  margin-bottom: 48px;
}
#components-layout-demo-basic > .ant-layout:last-child {
  margin: 0;
}
</style>
