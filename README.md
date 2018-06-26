## 前端移动端总结

### 1.点击样式闪动,当你点击一个链接或者通过Javascript定义的可点击元素的时候，它就会出现一个半透明的灰色背景。
根本原因是-webkit-tap-highlight-color，这个属性是用于设定元素在移动设备（如Adnroid、iOS）上被触发点击事件时，响应的背景框的颜色。建议写在样式初始化中以避免所以问题：div,input(selector) {-webkit-tap-highlight-color: rgba(0,0,0,0);}另外出现蓝色边框：outline:none；

### 2.屏蔽用户选择
禁止用户选择页面中的文字或者图片
```css
-webkit-touch-callout: none;
-webkit-user-select: none;
-khtml-user-select: none;
-moz-user-select: none;
-ms-user-select: none;
user-select: none;
```
### 移动端如何清除输入框内阴影
在iOS上，输入框默认有内部阴影，但无法使用 box-shadow 来清除，如果不需要阴影，可以这样关闭：
```css
-webkit-appearance: none;
```

### 禁止文本缩放
```css
-webkit-text-size-adjust: 100%;
```

### 如何禁止保存或拷贝图像
```css
img{-webkit-touch-callout: none;}
```

### 解决字体在移动端比例缩小后出现锯齿的问题
```css
-webkit-font-smoothing: antialiased;
```

### 设置input里面placeholder字体的大小
```css
::-webkit-input-placeholder{ font-size:10pt;}
```

### 移动端去除type为number的箭头
```css
input::-webkit-outer-spin-button,input::-webkit-inner-spin-button{      

    -webkit-appearance: none !important;     

    margin: 0;   

}
```
