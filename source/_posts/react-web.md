---
  title: react-web
---

### 示例项目
  
  1. 一个基于material-ui的react的 实例项目
    [查看](http://www.yangyun.fun:8001)

### 简介

   react是facebook 开源的一套前端开源框架,在react里一切皆组件,它通过虚拟DOM的方式进行

### 基本的用法

1. class 模式

   template

   ```
     import React from 'react'
      class A extends React.Component{
        render(){
           return(
             <div>
             </div>
           )
    
        }
      }
  ```

生命周期
  

2. hooks 模式(函数式)

   template

   ```
    import React from 'react';
    function A(){
      return (
        <div>

        </div>
      )
    }

 生命周期

   ```
   React.useEffect(()=>{
     // 初始化执行

   },[state])//