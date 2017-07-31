
# 以下是该部分所需API
# 获取用户公众号菜单信息
**简要描述：** 
> 获取公众号用户授权,返回用户公众号信息以及菜单信息

**请求URL：** 
- 
  
**请求方式：**
- POST 

**request传入参数：** 

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|custcert |是  |string |租户id   |
|userinfo |是  |string | 用户信息    |
|—usercode |是  |string | 用户的编号    |

**response返回参数说明：** 

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|code |是  |string |0失败 1成功   |
|msg |是  |string | 失败描述信息    |
|button |是  |数组 | 微信公众号一级菜单信息  |
|-type |是  |string | 菜单栏点击展示类型  |
|-name |是  |string | 菜单栏名称  |
|-url |是  |string |type为view时展示网页的url |
|-subbutton |是  |数组 | 二级菜单信息  |
 **返回示例**
入参
``` 
{
    'custid':'1',
    'userinfo':{
        'usercode':'452'
    }
},

```
**返回示例**
出参
``` 
  {
    "code": 1,
    "msg":'',
    button":[
      { 
          "type":"view",
          "name":"xxx",
          "url":"xxx"
      },
      {
           "name":"xxx",
           "sub_button":[
           {    
               "type":"view",
               "name":"xxx",
               "url":"http://www.soso.com/"
            },
            {
                 "type":"view",
                 "name":"xxx",
                 "url":"xxx",
             },
           ]
       }]
  }
```
 **备注** 

- 更多返回错误代码请看首页的错误代码描述

---
# 返回微信公众号修改菜单栏信息
**简要描述：** 

> 用户自定义完成菜单栏,将修改菜单栏信息组装成json格式字符串返回至后台

**请求URL：** 

  
**请求方式：**
- POST 

**request传入参数：** 

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|custcert |是  |string |租户id   |
|userinfo |是  |string | 用户信息    |
|—usercode |是  |string | 用户的编号    |
|button |是  |数组 | 修改后微信公众号一级菜单信息  |
|-type |是  |string | 修改后菜单栏点击展示类型  |
|-name |是  |string | 修改后菜单栏名称  |
|-url |是  |string |type为view时修改展示网页的url |
|-subbutton |是  |数组 | 修改二级菜单信息  |

**response返回参数说明：** 

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|code |是  |string |0失败 1成功   |
|msg |是  |string | 失败描述信息    |

 **返回示例**
 入参
``` 
{
    'custid':'1',
    'userinfo':{
        'usercode':'452'
    },
    button":[
      { 
          "type":"view",
          "name":"xxx",
          "url":"xxx"
      },
      {
           "name":"xxx",
           "sub_button":[
           {    
               "type":"view",
               "name":"xxx",
               "url":"http://www.soso.com/"
            },
            {
                 "type":"view",
                 "name":"xxx",
                 "url":"xxx",
             },
           ]
       }]
},
```
 **返回示例**
 出参
``` 
{
    "code": 1,
     "msg":'',
},
```



 **备注** 

- 更多返回错误代码请看首页的错误代码描述




---

# 自定义微信公众号菜单获取展示报表信息
**简要描述：** 

> 微信公众号用户自定义菜单,通过post请求报表信息,让用户选择展示已有报表

**请求URL：** 
- 
  
**请求方式：**
- POST 

**参数：** 

**request传入参数：** 

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|custcert |是  |string |租户id   |
|userinfo |是  |string | 用户信息    |
|—usercode |是  |string | 用户的编号    |

**response返回参数说明：** 

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|code |是  |string |0失败 1成功   |
|msg |是  |string | 失败描述信息    |
|reportsinfo |是  |数组 | 报表信息  |
|-name |是  |string | 报表名称|
|-url |是  |string |报表资源位置|


**返回示例**
入参
``` 
{
    'custid':'1',
    'userinfo':{
        'usercode':'452'
    }
},

```
**返回示例**
出参
``` 
  {
    "code": 1,
    "msg":'',
    "reportsinfo":[
        {
            "name":"xxx",
            "url":"xxx"
        },
        {
            "name":"xxx",
            "url":"xxx"
        }
    ]
  }
```

 **备注** 

- 更多返回错误代码请看首页的错误代码描述

---

# 2017年7月26日14:48:50



# 实现了整个大体样式与结构,正在实现"编辑"-"删除"的弹出框---

# 实现了"编辑"-的弹出框--- 2017年7月27日17:11:04

### 下一步实现 "删除的弹出框"~~~~~~~~~

# 实现"删除的弹出框"
### 下一步实现"添加一级按钮事件"ing~~~

## 大致实现添加事件,
  bug1: 新增一级菜单按钮,再新增二级菜单按钮会出现bug,只有将整个按钮删除才能实现..> 因为整个一级菜单最多只有三个,所以bug没了.....

## 完成了整个修改微信菜单的结构与样式以及获取了相关数据,

   