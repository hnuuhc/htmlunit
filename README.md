HtmlUnit封装
===============

### 说明:

1.对一些HtmlUnit工具进行包装,开箱即食,代码风格一致,参数可直接相互使用  
2.在发送网络错误时可以重试  
3.默认配置已经可以应对大部分网站,无需设置过多参数

### 简单示例:

```
Document doc = HtmlUnitUtil.connect("https://www.baidu.com")
.proxy(proxyHost, proxyPort) // or socks() 设置代理  
.retry(MAX_RETRY, MILLISECONDS_SLEEP) // 重试次数，重试等待间隔   
.get().parse(); // post() or execute() or get().json()
```

## 鸣谢

感谢[**JetBrains**](https://www.jetbrains.com/zh-cn/community/opensource/#support)提供的开源开发许可证，JetBrains 通过为核心项目贡献者免费提供一套一流的开发者工具来支持非商业开源项目。

[<img src="https://www.jetbrains.com/icon.svg" width="200"/>](https://www.jetbrains.com/zh-cn/community/opensource/#support)
