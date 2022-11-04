# 请注意，该项目不再维护

* * *

[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-LoadingIndicatorView-green.svg?style=flat)](https://android-arsenal.com/details/1/2686)

加载指示器视图 LoadingIndicatorView
===================

> **现在LoadingIndicatorView已将版本更新为2。如果您对本库有任何问题或建议，欢迎告诉我！**

## 简介
LoadingIndicatorView是一个不错的Android加载动画的集合。

你也可以在这里找到[iOS版本](https://github.com/ninjaprox/NVActivityIndicatorView) 

## 演示
![avi](screenshots/avi.gif)

## 用法

### 第一步

在build.gradle中添加依赖项
```groovy
    dependencies {
       compile 'com.wang.avi:library:2.1.3'
    }
```

### 第二步

将LoadingIndicatorView添加到布局中:

Simple

```java
    <com.wang.avi.LoadingIndicatorView
        android:layout_width="wrap_content"  
        android:layout_height="wrap_content"
        app:indicatorName="BallPulseIndicator"
        />
```

Advance

```java
    <com.wang.avi.LoadingIndicatorView
        android:id="@+id/avi"
        android:layout_width="wrap_content"  //or your custom size
        android:layout_height="wrap_content"  //or your custom size
        style="@style/LoadingIndicatorView"// or LoadingIndicatorView.Large or LoadingIndicatorView.Small
        android:visibility="visible"  //visible or gone
        app:indicatorName="BallPulseIndicator"//Indicator Name
        app:indicatorColor="your color"
        />
```

### 第三步

它的使用非常简单

```java
   void startAnim(){
        avi.show();
        // or avi.smoothToShow();
   }
   
   void stopAnim(){
        avi.hide();
        // or avi.smoothToHide();
   }
   
```

## 自定义指示器
参见示例中的 [MyCustomIndicator](https://gitee.com/tcxx726/LoadingIndicatorView/blod/master/app/src/main/java/com/example/LoadingIndicatorView/MyCustomIndicator.java) 

## 代码混淆

使用proguard时需要添加规则:

```
-keep class com.wang.avi.** { *; }
-keep class com.wang.avi.indicators.** { *; }
```

指示器是从类名中加载的，proguard可能会改变它(重命名)

## 指标

如**演示**中所示，指标如下:

**第1行**
 * `BallPulseIndicator`
 * `BallGridPulseIndicator`
 * `BallClipRotateIndicator`
 * `BallClipRotatePulseIndicator`

**第2行**
 * `SquareSpinIndicator`
 * `BallClipRotateMultipleIndicator`
 * `BallPulseRiseIndicator`
 * `BallRotateIndicator`

**第3行**
 * `CubeTransitionIndicator`
 * `BallZigZagIndicator`
 * `BallZigZagDeflectIndicator`
 * `BallTrianglePathIndicator`

**第4行**
 * `BallScaleIndicator`
 * `LineScaleIndicator`
 * `LineScalePartyIndicator`
 * `BallScaleMultipleIndicator`

**第5行**
 * `BallPulseSyncIndicator`
 * `BallBeatIndicator`
 * `LineScalePulseOutIndicator`
 * `LineScalePulseOutRapidIndicator`

**第6行**
 * `BallScaleRippleIndicator`
 * `BallScaleRippleMultipleIndicator`
 * `BallSpinFadeLoaderIndicator`
 * `LineSpinFadeLoaderIndicator`

**第7行**
 * `TriangleSkewSpinIndicator`
 * `PacmanIndicator`
 * `BallGridBeatIndicator`
 * `SemiCircleSpinIndicator`
 
**第8行**
 * `com.wang.avi.sample.MyCustomIndicator`

## 感谢
- [NVActivityIndicatorView](https://github.com/ninjaprox/NVActivityIndicatorView)
- [Connor Atherton](https://github.com/ConnorAtherton)

## 联系我

如果你对这个项目有更好的想法或方法，请让我知道，谢谢:)

[Email](mailto:1094877764@qq.com)

[微博](http://weibo.com)

[Blog](http://weibo.com)

### 许可证
```
Copyright 2015 jack wang

根据Apache许可证2.0版许可(“许可证”)；除非符合许可证的规定，否则您不得使用本文件。您可以从以下网址获得许可证的副本

   http://www.apache.org/licenses/LICENSE-2.0

除非适用法律要求或书面同意，软件在许可证下分发是在“原样”的基础上分发的，没有任何明示或暗示的保证或条件。有关管理权限和的特定语言，请参见许可证许可证下的限制。
```

