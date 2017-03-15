# vue_ueditor
vue2集成百度ueditor

使用方法<br>
  
<Ueditor @ready="editorReady" style="width: 500px;height: 440px;"></Ueditor>

     
methods: {
      editorReady (instance) {
        instance.setContent('');
        instance.addListener('contentChange', () => {
          this.content = instance.getContent();
        });
      },
    },
