# vue-next-slider-vertify


## 介绍

基于 Vue3 的滑动验证码组件

## 软件架构

vue3

## 安装教程

- yarn

  - yarn add vue-next-slider-vertify

- npm
  - npm i vue-next-slider-vertify

## 使用说明

```js
// script
import SliderVertify from 'vue-next-slider-vertify'

// template
<SliderVertify />

// style
@import url('vue-next-slider-vertify/lib/style.css');
```

## 属性 & 事件

```js
export interface SliderVertifyProps {
  /**
   * @description   canvas宽度
   * @default       320
   */
  width?: number
  /**
   * @description   canvas高度
   * @default       160
   */
  height?: number
  /**
   * @description   滑块边长
   * @default       42
   */
  l?: number
  /**
   * @description   滑块半径
   * @default       9
   */
  r?: number
  /**
   * @description   是否可见
   * @default       true
   */
  visible?: boolean
  /**
   * @description   滑块文本
   * @default       向右滑动滑块完成拼图
   */
  text?: string
  /**
   * @description   刷新按钮icon, 为icon的url地址
   * @default       -
   */
  refreshIcon?: string
  /**
   * @description   用于获取随机图片的url地址
   * @default       https://picsum.photos/${id}/${width}/${height}, 具体参考https://picsum.photos/, 只需要实现类似接口即可
   */
  imgUrl?: string
  /**
   * @description   拖拽滑块时的回调, 参数为当前滑块拖拽的距离
   */
  onDraw?(l: number): void
  /**
   * @description   用户的自定义验证逻辑
   */
  onCustomVertify?(arg: VertifyType): VertifyType
  /**
   * @description   验证成功回调
   */
  onSuccess?(): void
  /**
   * @description   验证失败回调
   */
  onFail?(): void
  /**
   * @description   刷新时回调
   */
  onRefresh?(): void
}

```

## 效果展示
- 默认状态

<img src="https://s1.ax1x.com/2022/06/23/jCTkLQ.png" alt="jCTkLQ.png" border="0">

- 成功

<img src="https://s1.ax1x.com/2022/06/23/jCTFsg.png" alt="jCTFsg.png" border="0">

- 失败

<img src="https://s1.ax1x.com/2022/06/23/jCTEZj.png" alt="jCTEZj.png" border="0">


## 参考

[React 滑动验证组件](https://www.npmjs.com/package/react-slider-verify)
