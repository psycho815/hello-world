记录日常工作中所遇到的bug
###mobile
1. 问题：选择框select在mac系统点击无效。

原因：select的高度设置失效
解决：不要在select元素选择器上写样式，改为其class样式即可。

2. 问题：input在手机端展现不一样，高度变高，出现圆角

原因：未重置默认样式
解决：设置padding:0; border-radius:0;

3. 问题：手机浏览器横屏字体被放大；

解决：在body设置属性-webkit-text-size-adjust: none;

  1、当样式表里font-size<12px时，中文版chrome浏览器里字体显示仍为12px，这时可以用  html{-webkit-text-size-adjust:none;}
  2、-webkit-text-size-adjust放在body上会导致页面缩放失效
  3、body会继承定义在html的样式
  4、用-webkit-text-size-adjust不要定义成可继承的或全局的
