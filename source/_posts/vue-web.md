---
   title: "Vue 理解和项目创建"
---

### Vue的发展
   vue 是开源的基于前端页面的mvvm框架,主要用于构建网站或者app，其原理可以访问 [vue 官网](https://cn.vuejs.org/)，或者是 [github 地址](https://github.com/vuejs/vue),由于其学习成本低，开发效率高，逐渐成为了广大开发者的必备技能了，对于该框架无论对于后端开发人员或者是前端的开发人员，本人都觉得应该对其有一定的了解，若你是前端开发人员，那更应该要达到熟悉的程度;下面是本人的一个构建vue项目的流程简介

### 如何构建一个vue的项目

  ## 方法一
  直接引用

      ```
        <!DOCTYPE>
        <html>
            <head>
              <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
              <script>
                  var app=new Vue({
                     el:'#app',//挂载的dom
                     data:{ //绑定的数据
                        text:'msg'
                     },
                     //生命周期函数
                     beforeCreate:function(){}
                     created:function(){},
                     berforeMounted:fucntion(){},
                     beforeUpdate:function(){},
                     mounted:function(){},
                     beforeDestroy:function(){},
                     destroyed:function(){}
                  })
              </script>
            </head>
            <body>
               <div id="app">
               </div>
            </body>
        </html>
      ```
  ## 方法二 
该方法是通过nodejs环境进行构建的,所以需要安装, [安装地址](http://nodejs.cn/)
    步骤如下
    以下是终端操作
   1.  配置npm镜像

      ```
        npm config set registry https://registry.npm.taobao.org
      ```
   2. 全局安装vue/cli3
      ```
        npm  install -g  @vue/cli
      ```
   3. 执行cli3 的创建命令  
     ```
       vue ui
     ``` 
   4. 如下图
     ![](/images/vueui.PNG)
