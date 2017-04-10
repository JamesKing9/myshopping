# TOC



# myeclipse







# Eclipse-Java EE

## 一、新建

1、New > "Dynamic Web Project"

2、然后输入“Project name”，选择“Target runtime”，这里选择`Apache Tomcat v6.0`，其他默认。

3、一路`Next`，中间可以自定义`Content directory`



## 二、添加项目的执行逻辑

上面3步完成后，就可以在`WEB-INF`目录下写 jsp 格式的文件了。

然后在项目的根目录下写`index.jsp`文件，定向跳转的页面`<jsp:forward page="WEB-INF/login.jsp"></jsp:forward>`

index.jsp 的完整代码

```jsp
<%@ page language="java" contentType="text/html; charset=utf-8"
    pageEncoding="utf-8"%>
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=ISO-8859-1">
<title>Insert title here</title>
</head>
<body>
	<jsp:forward page="WEB-INF/login.jsp"></jsp:forward>
</body>
</html>
```

有 2 点要注意：

1. 指定文本的编码和该页面的编码为`utf-8`;
2. 使用`<jsp:forward page="WEB-INF/login.jsp"></jsp:forward>`

来完成跳转。



## 三、将项目通过服务器部署到Web（网）上

第一次时要配置服务器。

`Define a New Server`  > `Select the server type: "Tomcat v6.0 Server"`

将可用的资源配置到Server 上：

`Available` -> `Configured`

然后就可以`Finish`了。

在`Server`列表中，`Start` 配置好的`server`，将项目通过服务器部署到Web（网）上。



