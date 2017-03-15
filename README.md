# vue_ueditor
vue2集成百度ueditor<br>
###使用方法<br>
[我的博客](http://www.cnblogs.com/cshhs/p/6555398.html)  
<Ueditor @ready="editorReady" style="width: 500px;height: 440px;"></Ueditor>

```javascript    
methods: {
    editorReady (instance) {
        instance.setContent('');
        instance.addListener('contentChange', () => {
            this.content = instance.getContent();
        });
    },
    },
```
