# Canvas

## 绘制圆弧

  > 绘制圆弧

    Context.arc(x, y, radius,startAngle,endAngle, anticlockwise)
      x:  圆弧中心（圆心）的 x 轴坐标。
      y:  圆弧中心（圆心）的 y 轴坐标。
      radius: 圆弧的半径。
      startAngle: 圆弧的起始点， x轴方向开始计算，单位以弧度表示。
      endAngle: 圆弧的终点， 单位以弧度表示。
      anticlockwise: 可选的Boolean值 ，如果为 true，逆时针绘制圆弧，反之，顺时针绘制。 默认是false(顺时针)

    Context.arcTo(x1, y1, x2, y2, radius) --200,100,400,60,100  有兼容性问题
      x1:第一个控制点的X轴坐标
      y1:第一个控制点的Y轴坐标
      x2:第二个控制点的X轴坐标
      y2:第二个控制点的Y轴坐标
      radius: 圆弧的半径

  > 绘制扇形

    1.先确定画笔的起始点
    2.画圆弧
    3.关闭路径
    4.描边

## 绘制文字

  > 绘制填充文本

    context.fillText(text, x, y [, maxWidth]);
      text:使用当前的 font, textAlign, textBaseline 和 direction 值对文本进行渲染。
      x:文本起点的 x 轴坐标。
      y:文本起点的 y 轴坐标

  > 绘制描边文本

    context.strokeText(text, x, y [, maxWidth]);
      text:使用当前 font，textAlign，textBaseline和direction 的值对文本进行渲染。
      x:文本起始点的 x 轴坐标。
      y:文本起始点的 y 轴坐标。

  > 获取文本的宽度

    context.measureText(text);
      text: 需要测量的文本

  > 设置字体大小和文本字体

    context.font = value;
      value 默认字体是 10px sans-serif.

  > 设置文本的对齐方式

    ctx.textAlign = "left" || "right" || "center";
      left:文本左对齐。
      right:文本右对齐。
      center:文本居中对齐。
  > 设置文本的基线

    context.textBaseLine = bottom top

  > 设置文本的方向(没有实现)

    ctx.direction = "ltr" || "rtl" ;
      ltr:文本方向从左向右。
      rtl:文本方向从右向左

## 绘制图像

  > 把图像绘制在canvas

    void ctx.drawImage(image, dx, dy);
    void ctx.drawImage(image, dx, dy, dWidth, dHeight);
    void ctx.drawImage(image, sx, sy, sWidth, sHeight, dx, dy, dWidth, dHeight);
      image: 图片对象 --内置对象 new Object() new Date();
      dx:目标画布的左上角在目标canvas上 X 轴的位置。---图片距离canvas的左上角的X轴的坐标

      dy:目标画布的左上角在目标canvas上 Y 轴的位置。---图片距离canvas的左上角的Y轴的坐标

      dWidth:在目标画布上绘制图像的宽度。 允许对绘制的图像进行缩放。 如果不说明， 在绘制时图片宽度不会缩放。
              设置图片在canvas上显示多大
      dHeight:在目标画布上绘制图像的高度。 允许对绘制的图像进行缩放。 如果不说明， 在绘制时图片高度不会缩放。
              设置图片在canvas上显示多大
      sx:需要绘制到目标上下文中的，源图像的矩形选择框的左上角 X 坐标。
              选取的原来图片的左上角的位置的X轴
      sy:需要绘制到目标上下文中的，源图像的矩形选择框的左上角 Y 坐标。
              选取的原来图片的左上角的位置的Y轴
      sWidth:需要绘制到目标上下文中的，源图像的矩形选择框的宽度。如果不说明，整个矩形从坐标的sx和sy开始，到图像的右下角结束。
      剪切图像的大小
      sHeight:需要绘制到目标上下文中的，源图像的矩形选择框的高度。

## 变换

   所有变换都必须在绘制前去用 否则没有效果

  > 平移变换

     translate(x,y)

  > 旋转变换

    rotate(deg) //弧度

  > 缩放变换

    scale(sx,sy)

## 学会简单的echarts方法

    > 学会用echarts画折线图

    > 学会用echarts画饼状图