## 错误workaround

Microsoft.Azure.CognitiveServices.Vision.Face 的2.2.0-preview版本，如果在调用faceClient时候遇到了这个错误：
```
APIErrorException: 'Operation returned an invalid status code 'NotFound'' 
```

绕过这个错误的方式是在定义faceClient的Endpoint的时候去掉face/v1.0
例如，如下是我们从Azure Portal上获取的endpoint
https://eastasia.api.cognitive.microsoft.com/face/v1.0
当为faceClient.Endpoint赋值时：  
this.faceClient.Endpoint = "https://eastasia.api.cognitive.microsoft.com/";
