# vue_ueditor
vue2集成百度ueditor

使用方法
  <Ueditor @ready="editorReady" style="width: 500px;height: 440px;"></Ueditor>
  对应methods     
  methods: {
      editorReady (instance) {
        instance.setContent('');

        instance.addListener('contentChange', () => {
          this.content = instance.getContent();
        });
      },
    },
