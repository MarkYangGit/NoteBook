# EGE 的文字处理

设置字体样式  
 ```setfont() ```函数可以设置字体、宽度和高度，还可以将文字样式设置为斜体，粗体，旋转角度等。
  通常以如下方式使用，设置文字的高度和字体，宽度为0即让系统自动按照文字对应的宽度输出，如果设置固定宽度可能会让文字变形。常用字体有："宋体", "黑体", "楷体"等。
```C
setfont(height, 0, "字体名");
```

设置文字颜色：```setcolor(color)```

设置字体背景透明：```setbkmode(TRANSPARENT); //设置文字背景色为透明```

文字对齐方式：```settextjustify(CENTER_TEXT, CENTER_TEXT);```

文字输出
```C
xyprintf(x,y,text);

outtextxy(x, y, "要输出的文字");  //可以免去字符串解析。

rectprintf(x, y, width, height, "格式字符串", 参数1， 参数2，...);  //指定一个矩形区域，让文字即将超出区域时自动换行。
```

|	|单行输出|多行输出|
|----|----|----|
|固定文本|```outtextxy(), outtext()```|```outtextrect()```|
|格式化文本|```xyprintf()```|```rectprintf()```|

