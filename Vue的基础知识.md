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
- Vue绑定标签属性
  - v-bind:绑定标签的属性
  - v-model：表单项value的双向绑定
  - v-model.trim：去掉表单输入框前后的空格 

- 条件渲染和列表渲染
  - 条件渲染：v-if、v-else、v-show
  - 列表渲染：v-for = "(遍历出来的元素，下标) in 要遍历的数据模型" 
     ```
        <ul>
        <li v-for="(element,index) in elementList":value="index">{ {element} }</li>
        </ul>
     ```

- 常用事件绑定
  - 点击事件绑定：v-on：click
  - 鼠标移动事件绑定：v-on：mousemove
  - 阻止标签的默认行为：@click.prevent
  - 阻止事件冒泡：@click.stop

- Vue生命周期的钩子函数
    - 生命周期：一个对象从创建、初始化、工作再到释放、清理和销毁的全过程
    - 钩子函数：在生命周期特定时间点会自动执行的函数
    + beforeCreate：Vue对象创建之前执行
    + created：Vue对象创建完成时执行
    + beforeMount：Vue对象开始挂载数据时执行
    + mounted：Vue对象挂载数据完成时执行
    + beforeUpdate：Vue对象中的data数据发生改变之前执行
    + updated：Vue对象中的data数据发生改变后时执行
    + beforeDestroy：Vue对象被销毁之前执行
    + destroyed ：Vue对象销毁完成后执行
