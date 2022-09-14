# goods-card
# 使用方法

```vue
// 引入组件
import card  from 'zxzxj-goods-card'

<card
:link="`#/product/${item.id}`"
:goodsImg="item.picture"
:goodsName="item.name"
:goodsDescribe="item.desc"
:goodsPrice="item.price"
/>
// link: 跳转路径, 必须属性, 类型为字符串
// goodsImg: 商品图片, 必须属性, 类型为字符串
// goodsName: 商品名字, 必须属性, 类型为字符串
// goodsDescribe: 商品描述, 必须属性, 类型为字符串
// goodsPrice: 商品价格, 必须属性, 类型为字符串或者数字
```

#### 效果

![](Snipaste_2022-09-14_18-59-14.png)
