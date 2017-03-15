# vue_ueditor
vue2集成百度ueditor<br><br><br>
## 使用方法<br>
[我的博客](http://www.cnblogs.com/cshhs/p/6555398.html)  
<br><br>
```javascript 
<Ueditor @ready="editorReady" style="width: 500px;height: 440px;"></Ueditor>
```
<br><br><br>

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
