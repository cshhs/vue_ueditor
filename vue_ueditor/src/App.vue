<template>
  <div id="app">
    vue_ueditor
    <div>
      //此时监听子组件的事件,编辑器实例回调
      <Ueditor @ready="editorReady" style="width: 500px;height: 440px;"></Ueditor>
    </div>

  </div>
</template>

<script>
  import Ueditor from './components/Ueditor'

  export default {
    data(){
      return{
        content:''
      }
    },
    name: 'app',
    components: {
      Ueditor
    },
    methods: {
      editorReady (instance) {
        instance.setContent('');

        instance.addListener('contentChange', () => {
          this.content = instance.getContent();
        });
      },
    },
  }
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>
