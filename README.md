# BootstrapWebTest


## Bootstrap 单独样式类的使用技巧
- hidden-系列 指定在不同屏幕尺寸下含有该类的元素的隐藏
- visibility-系列 指定在不同屏幕尺寸下含有该类的元素的显示
- text-align系列 直接指定文字水平居中
- fade in系列 指定元素的过渡动画



## 自定义字体图标


[icomoon字体制作网站]: https://icomoon.io/

通过上述网站将生成的字体文件引入本地



再使用`@font-face` 在css文件中如下定义，*src*中严格按照格式引入四种不同类型文件

```css

@font-face {
  font-family: "icomoon";
  src: url("../icomoon-fonts/fonts/icomoon.eot") format("embedded-opentype"),
    url("../icomoon-fonts/fonts/icomoon.svg") format("svg"),
    url("../icomoon-fonts/fonts/icomoon.ttf") format("truetype"),
    url("../icomoon-fonts/fonts/icomoon.woff") format("woff");
}
```

在html中使用该字体

```html
<span class="ico-logo"></span>
<span class="ico-weijinsuo"></span>
```

在css中使用该字体

```css
.ico-logo::before {
  font-family: icomoon;
  content: "\e900";
  color: #e92322;
  font-size: 32px;
}
.ico-weijinsuo::before {
  font-family: icomoon;
  content: "\e901";
  font-size: 22px;
  color: #333;
}

```


