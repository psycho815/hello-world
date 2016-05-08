#mobile
*注意：此页面css3属性均只列出-webkit前缀*
**一.head**

    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0, user-scalable=0"/>

**二.reset**

    font-family: "Helvetica Neue", Helvetica, STHeiTi, sans-serif; /* 使用无衬线字体，应用于body */
    -webkit-touch-callout: none; /* 禁止长按链接与图片弹出菜单，应用于a,img */
    -webkit-user-select: none; /* 禁止选中文本（如无文本选中需求，必须)，应用于html,body */
    ::-webkit-selection { background:#FFF; color:#333;} /* 设置选中文本背景 */
    -webkit-tap-highlight-color: rgba(240,240,240,0.7); /* 设置点击背景框颜色 */
    -webkit-tap-highlight-color: rgba(0,0,0,0); /* 去掉点击背景 */
    -webkit-appearance:none /*表单控件样式重置 */

**三.bug**

1.问题：选择框select在mac系统点击无效。
原因：select的高度设置失效
解决：不要在select元素选择器上写样式，改为其class样式即可。

2.问题：input在手机端展现不一样，高度变高，出现圆角
原因：未重置默认样式
解决：设置padding:0; border-radius:0;

3.问题：手机浏览器横屏字体被放大；
解决：在body设置属性-webkit-text-size-adjust: none;

    1、当样式表里font-size<12px时，中文版chrome浏览器里字体显示仍为12px，这时可以用  html{-webkit-text-size-adjust:none;}
    2、-webkit-text-size-adjust放在body上会导致页面缩放失效
    3、body会继承定义在html的样式
    4、用-webkit-text-size-adjust不要定义成可继承的或全局的
