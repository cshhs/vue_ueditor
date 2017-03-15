# vue_ueditor
vue2集成百度ueditor<br><br>
## 使用方法<br>

```javascript
关于上传图片可以在ueditor.config.js里面的serverUrl进行配置
// 服务器统一请求接口路径 类似下面 亲测完全可以使用，在本地测试会有延迟
打包之后放置到服务器上面速度即可恢复正常
serverUrl: 'http://xxx.com/Public/Home/ueditor/php/controller.php',
```

相关详情可以查看[我的博客](http://www.cnblogs.com/cshhs/p/6555398.html)  

```javascript 
<Ueditor @ready="editorReady" style="width: 500px;height: 440px;"></Ueditor>
```

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
