# 获取App配置插件(WorkPlus_LightApp)
---

## 1. 获取app请求的api地址
>获取app请求的api地址

请求调用示例:

```javascript
function getConfig(){
 cordova.exec(function(result) {
            alert(JSON.stringify(result, null, 4));
        },
        function(error) {
            alert("调用失败");
        },
        "WorkPlus_LightApp",
        "getConfig", 
        ["shakeUrl", "colleagueCircleUrl",...]
        );
}

说明：
请求输入数据：

根据需要的配置传入如下参数：shakeUrl（摇一摇地址），colleagueCircleUrl（同事圈地址）， _ApiUrl（轻应用管理后台地址）， _AdminUrl（管理平台地址），scheduleUrl（日程管理地址）；

请求返回数据：

根据传入的参数, 决定返回的数据
{
	"shakeUrl":"xxx",
	"colleagueCircleUrl":"xxx",
	.....,
	“status”: 0
}
```

<br/>