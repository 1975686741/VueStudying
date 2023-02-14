# 动画(transiton)
- vue要实现动画很简单, 同时他提供了很多种实现方式, 为了快速入门, 这里只讲一种最简单实用的方法, 就是结合animate.css这个css动画库.
- 准备工作
  安装animate.css
  `npm install animate.css --save`
  在main.js中导入animate.css, 这样相当于到所有页面都能使用他的样式.
  `import animate.css`
- <transition>
  vue的动画组件, 只需要用"<transition>"包裹要添加动画的元素(或组件), 这里我们要注意的就是触发条件:
  被包裹组件(或元素)上的v-if的值发生变化.
  被包裹组件(或元素)上的v-show的值发生变化.
  动态组件的is值发生变化的时候也会触发动画, 动态组件在业务代码中不常见,  记住这个名词即可.
 ` <template>
  <button @click="isShow = !isShow">切换</button>

  <transition
    :duration="1000"
    enter-active-class="animate__animated animate__fadeInDown"
    leave-active-class="animate__animated animate__fadeOutUp"
    >
    <p v-if="isShow">hello</p>
  </transition>
  </template>

  <script>
  import "animate.css";
  import { defineComponent } from "vue";
  export default defineComponent({
    data() {
      return {
        isShow: true,
      };
    },
  });
  </script>
 `
