# 图形绘制

### acr()
#### 功能：这个函数用于画圆弧。边线颜色由setcolor函数决定
声明：
```C
void arc(
    int x,   //横坐标
    int y,   //纵坐标
    int stangle,   //圆弧的起始角的角度。
    int endangle,   //圆弧的终止角的角度。
    int radius,    //圆弧半径
    PIMAGE pimg = NULL
);
void arcf(
    float x,
    float y,
    float stangle,
    float endangle,
    float radius,
    PIMAGE pimg = NULL
);
```
---
### bar()
### 功能：这个函数用于画无边框填充矩形。其中，填充颜色由setfillcolor函数决定
声明：
```C
void bar(
    int left,   //矩形左部 x 坐标。
    int top,    //矩形上部 y 坐标。
    int right,   //矩形右部 x 坐标（该点取不到，实际右边界为right-1）。
    int bottom,    //矩形下部 y 坐标（该点取不到，实际下边界为bottom-1）。
    PIMAGE pimg = NULL
);
```
---

### bar3d()
#### 功能：这个函数用于画有边框三维填充矩形。其中，填充颜色由setfillcolor函数决定
声明：
```C
void bar3d(
    int left,
    int top,
    int right,
    int bottom,
    int depth,   //矩形深度。
    bool topflag,  ///为 false 时，将不画矩形的三维顶部。该选项可用来画堆叠的三维矩形。
    PIMAGE pimg = NULL
);
```

示例：
```C
#include "graphics.h"

int main()
{
    initgraph(600, 400);
    setfillstyle(RED);
    bar3d(100, 100, 150, 150, 20, 1);
    getch();
    return 0;
}
```
---
### circle
#### 功能：这个函数用于画圆。此圆是空心的，不填充，而边线颜色由setcolor函数决定
声明：
```
void circle(
    int x,
    int y,
    int radius,
    PIMAGE pimg = NULL
);
void circlef(
    float x,
    float y,
    float radius,
    PIMAGE pimg = NULL
);
```
---
### drawpoly()
#### 功能：这个函数用于画多边形。边线颜色由setcolor函数决定

声明：
```c
void drawpoly(
    int numpoints, ///多边形点的个数。
    const int *polypoints,  //polypoints每个点的坐标（依次两个分别为x,y），数组元素个数为 numpoints * 2。
    PIMAGE pimg = NULL
);
//该函数并不会自动连接多边形首尾。如果需要画封闭的多边形，请将最后一个点设置为与第一点相同。
```






