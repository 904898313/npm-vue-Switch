# switch开关组件 -- 使用方法

# 参数说明
## @param value.sync
* 说明：双向绑定的switch开关值
* 是否必传：是
* 值类型：Boolean
* 注意：传值需要带上.sync，用于通过子组件触发修改父组件中的值

## @param on
* 说明：设置switch开关值为true时的样式
* 是否必传：否
* 值类型：Object
* 参数说明{
  text: 'on',         // 文案描述,默认值:`on`,如:`开启`
  textStyle: '',      // 文案描述样式,如:`color:red;`
  containerStyle: '', // 开关容器样式,如:`width:100px;border:0px;`
  dotsStyle: ''       // 圆点样式,如:`width:20px;margin-left: calc(100% - 20px);`
}
* 注意：组件圆点移动用参数的`dotsStyle`的`margin-left: calc(100% - 20px)`,此css实现圆点移动。 必须将此字段的偏移量设置为与圆点自身的width相同。如：圆点`width:50px`,应该设置`margin-left: calc(100% - 50px);`

## @param off
* 说明：设置switch开关值为false时的样式
* 是否必传：否
* 值类型：Object
* 参数说明{
  text: 'on',         // 文案描述,默认值:`on`,如:`开启`
  textStyle: '',      // 文案描述样式,如:`color:red;`
  containerStyle: '', // 开关容器样式,如:`width:100px;border:0px;`
  dotsStyle: ''       // 圆点样式,如:`width:20px;`,为false时无特殊需求,不需要设置`margin-left`
}

## @param disabled
* 说明：设置组件是否禁用
* 是否必传：否
* 值类型：Boolean

# 事件说明
## @event automaticChange
* 说明：switch开关值被异步改变时的回调函数
* 回调参数：改变后的Boolean值

## @event change
* 说明：手动切换switch开关值的回调函数
* 回调参数：改变后的Boolean值

```js
//main.js
import switchDom from 'ycg-vue-switch';
Vue.use(switchDom)
```
```html
<!-- html -->
<switch-dom
  :value.sync="val"
  :disabled="false"
  @change='change'
/>
```
off:<img width="77" alt="企业微信截图_16467074345146" src="https://user-images.githubusercontent.com/67309600/157156031-6371f04f-f01c-4665-8a3a-cdfdf9c587d2.png">
on:<img width="75" alt="企业微信截图_16467074413650" src="https://user-images.githubusercontent.com/67309600/157156049-a6ce33c7-6cb5-4efc-b536-d7b3ecc9591a.png">
