# 介绍

通常用于小程序中图片的展示，增强版的 image 标签，提供多种图片填充模式，支持图片懒加载、加载中提示、加载失败提示。

### Props

| 参数                   | 说明                                 | 类型             | 默认值     |
| ---------------------- | ------------------------------------ | ---------------- | ---------- |
| src                    | 图片链接                             | string           | -          |
| mode                   | 图片填充模式                         | string           | aspectFill |
| webp                   | 解析 webp 格式                       | boolean          | true       |
| width                  | 宽度，默认单位为`rpx`                | string           | -          |
| height                 | 高度，默认单位为`rpx`                | string           | -          |
| radius                 | 圆角大小，默认单位为`px`             | string ｜ number | 0          |
| round                  | 是否显示为圆形                       | boolean          | false      |
| lazy-load              | 是否懒加载                           | boolean          | false      |
| show-error             | 是否展示图片加载失败提示             | boolean          | true       |
| show-loading           | 是否展示图片加载中提示               | boolean          | true       |
| use-error-slot         | 是否使用 error 插槽                  | boolean          | false      |
| use-loading-slot       | 是否使用 loading 插槽                | boolean          | false      |
| show-menu-by-longpress | 是否开启长按图片显示识别小程序码菜单 | boolean          | false      |

### 图片填充模式 

| 合法值       | 说明                                                                                                                                 |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| scaleToFill  | 缩放模式，不保持纵横比缩放图片，使图片的宽高完全拉伸至填满 image 元素                                                                |
| aspectFit    | 缩放模式，保持纵横比缩放图片，使图片的长边能完全显示出来。也就是说，可以完整地将图片显示出来。                                       |
| aspectFill   | 缩放模式，保持纵横比缩放图片，只保证图片的短边能完全显示出来。也就是说，图片通常只在水平或垂直方向是完整的，另一个方向将会发生截取。 |
| widthFix     | 缩放模式，宽度不变，高度自动变化，保持原图宽高比不变                                                                                 |
| heightFix    | 缩放模式，高度不变，宽度自动变化，保持原图宽高比不变                                                                                 |
| top          | 裁剪模式，不缩放图片，只显示图片的顶部区域                                                                                           |
| bottom       | 裁剪模式，不缩放图片，只显示图片的底部区域                                                                                           |
| center       | 裁剪模式，不缩放图片，只显示图片的中间区域                                                                                           |
| left         | 裁剪模式，不缩放图片，只显示图片的左边区域                                                                                           |
| right        | 裁剪模式，不缩放图片，只显示图片的右边区域                                                                                           |
| top left     | 裁剪模式，不缩放图片，只显示图片的左上边区域                                                                                         |
| top right    | 裁剪模式，不缩放图片，只显示图片的右上边区域                                                                                         |
| bottom left  | 裁剪模式，不缩放图片，只显示图片的左下边区域                                                                                         |
| bottom right | 裁剪模式，不缩放图片，只显示图片的右下边区域                                                                                         |

### Slots

| 名称    | 说明                       |
| ------- | -------------------------- |
| loading | 自定义加载中的提示内容     |
| error   | 自定义加载失败时的提示内容 |

### Events

| 事件名     | 说明                       | 回调参数     |
| ---------- | -------------------------- | ------------ |
| bind:click | 点击图片时触发             | event: Event |
| bind:load  | 自定义加载失败时的提示内容 | event: Event |
| bind:error | 图片加载失败时触发         | event: Event |