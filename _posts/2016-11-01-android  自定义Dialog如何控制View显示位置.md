---
layout: post
title: android  自定义Dialog如何控制View显示位置
date:   2016-06-01 13:50:39
categories: others
---


## android  自定义Dialog如何控制View显示位置

重写Dialog，设置Dialog的contentView，如何设置contentView的现实位置，例子如下，设置ContentView底部显示

```
     WindowManager.LayoutParams lp = new WindowManager.LayoutParams();
     Window window = getWindow();
     lp.copyFrom(window.getAttributes());
     lp.width = WindowManager.LayoutParams.MATCH_PARENT;
     lp.height = WindowManager.LayoutParams.WRAP_CONTENT;
     lp.gravity = Gravity.BOTTOM;
     window.setAttributes(lp);
```

