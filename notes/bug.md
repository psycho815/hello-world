记录日常工作中所遇到的bug
###mobile
1. 问题：选择框select在mac系统点击无效。
原因：select的高度设置失效
解决：不要在select元素选择器上写样式，改为其class样式即可。

2. 问题：input在手机端展现不一样，高度变高，出现圆角
原因：未重置默认样式
解决：设置padding:0; border-radius:0;
