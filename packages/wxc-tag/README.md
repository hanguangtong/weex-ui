# wxc-tag 

> Weex通用标签组件，支持实心标签、空心标签、特殊标签、图片标签

## [Demo预览](https://h5.m.taobao.com/trip/wxc-tag/index.html?_wx_tpl=https%3A%2F%2Fh5.m.taobao.com%2Ftrip%2Fwxc-tag%2Fdemo%2Findex.native-min.js)
<img src="https://gw.alipayobjects.com/zos/rmsportal/hErVCTKqGcxNiyAmVWkp.gif" width="240"/>&nbsp;&nbsp;&nbsp;&nbsp;<img src="http://gtms01.alicdn.com/tfs/TB11omrSXXXXXagXVXXXXXXXXXX-200-200.png" width="160"/>

## 安装

```shell
npm i weex-ui --save
```

## 使用方法

```vue
<template>
  <div class="wrapper">
   <wxc-tag type="solid"
            tag-color="#ff5000"
            font-color="#ffffff"
            value="实心标签"></wxc-tag>
  </div>
</template>
<script>
  import { wxcTag } from 'weex-ui';
  export default {
    components: { wxcTag }
  };
</script>
```

- 更多数据格式可以参考 [demo/demo.data.js](https://github.com/alibaba/weex-ui/blob/master/example/tag/demo.data.js)
- 更多详细情况可以参考 [demo](https://github.com/alibaba/weex-ui/blob/master/example/tag/index.vue)


### 可配置参数

| Prop | Type | Required | Default | Description |
| ---- |:----:|:---:|:-------:| :----------:|
| **`type`** | `String` | `N` | `solid` | 标签的类型(注1) |
| **`value`** | `String` | `Y` | `` | 文字标签的文案 |
| **`tag-color`** | `String` | `N` | `#ff5000` | 标签颜色 |
| **`font-color`** | `String` | `N` | `#ffffff` | 文字颜色 |
| **`special-icon`** | `String` | `N` | `` | 特殊标签的小icon(注2) |
| **`img`** | `String` | `N` | `` | 图片类型tag的图片地址(注3) |

* 注1: type的类型有如下四种solid、hollow、special、image，默认是solid(实心)
* 注2: specialIcon本应该为iconfont的，但是考虑的Weex,直接使用png会更方便
* 注3: type为image时，img字段为必传
