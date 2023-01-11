- Vue的固定格式
     - “el”:”#区域的id”
     - “data”：需要定义的数据模型
     - “methods”：需要声明的函数
     - “watch”：添加监听 
     - ```
          <body>
           <div id="app">
           <div>{ {message} }</div>
            </div>
           <script>
             var vue = new Vue({
                "el":"#app",
           "data":{
            "message":"数据模型"
           },
          "methods"：{
               "函数名称":function(){
               //具体的业务操作
               }
             },
                 "watch":{
                    "监听的属性名称":function("监听的值"){
                      //具体的业务操作
                   }
                  }
            });
             </script>
           </body>
          ```
