---
title: CSS font-family 
tags:
- css
- font-family
categories:
- FE
---

## 起因

翻来覆去几回，还是觉得 [hexo-theme-cactus](https://github.com/probberechts/hexo-theme-cactus) 这款主题 简洁，干净的风格深得我心，或许是年纪大了吧。

但是这款主题的开发者不是国人，没有做中文适配，各大浏览器默认显示的是宋体阅读体验相当差，所以

## 现状

### Windows

在Windows下可选项不多，基本就宋体和微软雅黑，但是微软雅黑字号大了之后阅读体验就过山车般的下降

- **宋体（SimSun）**：Win下大部分游览器的默认字体，`宋体`在小字号下（如12px、14px）的显示效果还可以接受，但是字号一大就非常糟糕了，所以使用的时候要注意。
- **微软雅黑（"Microsoft Yahei"）**：从 Vista 开始，微软提供了这款新的字体，一款无衬线的黑体类字体，并且拥有 *Regular*、*Bold* 两种粗细的字重，显著提高了字体的显示效果。现在这款字体已经成为Windows游览器中最值得使用的中文字体。从Win8开始，`微软雅黑`又加入了 *Light* 这款更细的字重，对于喜欢细字体的设计、开发人员又多了一个新的选择。
- **Arial**：Win平台上默认的无衬线西文字体（为什么要说英文字体后面会解释），有多种变体，显示效果一般。
- **Tahoma**：十分常见的无衬线字体，被采用为Windows 2000、Windows XP、Windows Server 2003及Sega游戏主机Dreamcast等系统的预设字型，显示效果比`Arial`要好。
- **Verdana**：无衬线字体，优点在于它在小字上仍结构清晰端整、阅读辨识容易。
- **其他**：Windows 下默认字体列表：微软官网、维基百科、Office字体
- **结论：`微软雅黑`为Win平台上最值得选择的中文字体，但非游览器默认，需要设置；西文字体的选择以`Arial`、`Tahoma`等无衬线字体为主。**

### Linux

* **文泉驿点阵宋体**：类似`宋体`的衬线字体，一般不推荐使用。

* **文泉驿微米黑**：几乎是 Linux 社区现有的最佳简体中文字体。

### macOS & iOS

**华文黑体（STHeiti）、华文细黑（STXihei）**：属于同一字体家族系列，OS X 10.6 之前的简体中文系统界面默认字体，也是目前Chrome游览器下的默认字体，有 *Regular* 和 *Bold* 两个字重，显示效果可以接受，`华文细黑`也曾是我最喜欢的字体之一。

**黑体-简（Heiti SC）**：从 10.6 开始，`黑体-简`代替`华文黑体`用作简体中文系统界面默认字体，苹果生态最常用的字体之一，包括iphone、iPad等设备用的也是这款字体，显示效果不错，但是喇叭口设计遭人诟病。

**冬青黑体（ Hiragino Sans GB ）**：听说又叫`苹果丽黑`，日文字体`Hiragino KakuGothic`的简体中文版，简体中文有 *常规体* 和 *粗体* 两种，`冬青黑体`是一款清新的专业印刷字体，小字号时足够清晰，拥有很多人的追捧。

**Times New Roman**：Mac平台Safari下默认的字体，是最常见且广为人知的西文衬线字体之一，众多网页浏览器和文字处理软件都是用它作为默认字体。

**Helvetica、Helvetica Neue**：一种被广泛使用的传奇般的西文字体（这货还有专门的记录片呢），在微软使用山寨货的`Arial`时，乔布斯却花费重金获得了`Helvetica`苹果系统上的使用权，因此该字体也一直伴随着苹果用户，是苹果生态中最常用的西文字体。`Helvetica Neue`为`Helvetica`的改善版本，且增加了更多不同粗细与宽度的字形，共拥有51种字体版本，极大的满足了日常的使用。

**苹方（PingFang SC）**：在Mac OS X EL Capitan上，苹果为中国用户打造了一款全新中文字体--`苹方`，去掉了为人诟病的喇叭口，整体造型看上去更加简洁，字族共六枚字体：*极细体、纤细体、细体、常规体、中黑体、中粗体*。

**San Francisco**：同样是Mac OS X EL Capitan上最新发布的西文字体，感觉和`Helvetica`看上去差别不大，目前已经应用在Mac OS 10.11+、[ios](http://caibaojian.com/t/ios) 9.0+、watch OS等最新系统上。

**其他**：Mac下默认字体列表：苹果官网、维基百科

**iOS**:  *iOS系统的字体和Mac OS系统的字体相同，保证了Mac上的字体效果，iOS设备就没有太大问题。

**结论：目前`苹方`和`San Francisco`为苹果推出的最新字体，显示效果也最为优雅，但只有最新系统才能支持，而`黑体-简`和`Helvetica`可以获得更多系统版本支持，显示效果也相差无几，可以接受。**

### Android

**Droid Sans、Droid Sans Fallback**：`Droid Sans`为安卓系统中默认的西文字体，是一款人文主义无衬线字体，而`Droid Sans Fallback`则是包含汉字、日文假名、韩文的文字扩展支持。

**结论：`Droid Sans`为默认的字体，并结合了中英文，无需单独设置。**

## 实践

### 1. 字体的中英文写法

我们在操作系统中常常看到`宋体`、`微软雅黑`这样的字体名称，但实际上这只是字体的显示名称，而不是字体文件的名称，一般字体文件都是用英文命名的，如`SimSun`、`Microsoft Yahei`。在大多数情况下直接使用显示名称也能正确的显示，但是有一些用户的特殊设置会导致中文声明无效。
 **因此，保守的做法是使用字体的字体名称（英文）或者两者兼写。**如下示例：[·](http://caibaojian.com/font-family.html)

```
font-family: STXihei, "Microsoft YaHei";
font-family: STXihei, "华文细黑", "Microsoft YaHei", "微软雅黑";
```


### 2. 声明英文字体

绝大部分中文字体里都包含英文字母和数字，不进行英文字体声明是没有问题的，但是大多数中文字体中的英文和数字的部分都不是特别漂亮，所以建议也对英文字体进行声明。
**由于英文字体中大多不包含中文，我们可以先进行英文字体的声明，这样不会影响到中文字体的选择，因此优先使用最优秀的英文字体，中文字体声明则紧随其次。**如下示例：

```
font-family: Arial, "Microsoft YaHei";
```

### 3. 照顾不同的操作系统

- 英文、数字部分：在默认的操作系统中，Mac和Win都会带有`Arial`, `Verdana`, `Tahoma`等几个预装字体，从显示效果来看，`Tahoma`要比`Arial`更加清晰一些，因此字体设置`Tahoma`最好放到前面，当找不到`Tahoma`时再使用`Arial`；而在Mac中，还拥有一款更加漂亮的`Helvetica`字体，所以为了照顾Mac用户有更好的体验，应该更优先设置`Helvetica`字体；Android系统下默认的无衬线字体就可以接受，因此无需单独设置。**最后，英文、数字字体的最佳写法如下：**

```
font-family: Helvetica, Tahoma, Arial;
```

- 中文部分：在Win下，`微软雅黑`为大部分人最常使用的中文字体，由于很多人安装Office的缘故，Mac电脑中也会出现微软雅黑字体，因此把显示效果不错的`微软雅黑`加入到字体列表是个不错的选择；同样，为了保证Mac中更为优雅字体`苹方（PingFang SC）`、`黑体-简（Heiti SC）`、`冬青黑体（ Hiragino Sans GB ）`的优先显示，需要把这些字体放到中文字体列表的最前面；同时为了照顾到Linux操作系统的体验，还需要添加`文泉驿微米黑`字体。**最后，中文字体部分最佳写法如下：**

```
font-family: "PingFang SC", "Hiragino Sans GB", "Heiti SC", "Microsoft YaHei", "WenQuanYi Micro Hei";
```

**中英文整合写法：**

```
font-family: Helvetica, Tahoma, Arial, "Heiti SC", "Microsoft YaHei", "WenQuanYi Micro Hei";
font-family: Helvetica, Tahoma, Arial, "PingFang SC", "Hiragino Sans GB", "Heiti SC", "Microsoft YaHei", "WenQuanYi Micro Hei";
```

### 4. 注意向下兼容

如果还需要考虑旧版本操作系统用户的话，不得不加上一些旧版操作系统存在的字体：Mac中的`华文黑体`、`冬青黑体`，Win中的`黑体`等。**同样按照显示效果排列在列表后面，写法如下：**

```
font-family: Helvetica, Tahoma, Arial, "PingFang SC", "Hiragino Sans GB", "Heiti SC", STXihei, "Microsoft YaHei", SimHei, "WenQuanYi Micro Hei";
```

加入了` STXihei（华文细黑）`和` SimHei（黑体）`。

### 5. 补充字体族名称

字体族大体上分为两类：`sans-serif（无衬线体）`和`serif（衬线体）`，当所有的字体都找不到时，我们可以使用字体族名称作为操作系统最后选择字体的方向。一般非衬线字体在显示器中的显示效果会比较好，**因此我们需要在最后添加` sans-serif`，写法如下：**。

```
font-family: Helvetica, Tahoma, Arial, "PingFang SC", "Hiragino Sans GB", "Heiti SC", "MicrosoftYaHei", "WenQuanYi Micro Hei", sans-serif;
```

## 实践 *

### mi.com

```
14px/1.5 Helvetica Neue,Helvetica,Arial,Microsoft Yahei,Hiragino Sans GB,Heiti SC,WenQuanYi Micro Hei,sans-serif;
```

### juejin.im

```
font-family: -apple-system,system-ui,Segoe UI,Roboto,Ubuntu,Cantarell,Noto Sans,sans-serif,BlinkMacSystemFont,Helvetica Neue,PingFang SC,Hiragino Sans GB,Microsoft YaHei,Arial;
```

### cnodejs.org

```
font-family: "Helvetica Neue","Luxi Sans","DejaVu Sans",Tahoma,"Hiragino Sans GB",STHeiti,sans-serif!important;
}
```

### v2ex.com

```
font-family: "Helvetica Neue", "Luxi Sans", "DejaVu Sans", "Segoe UI", "Hiragino Sans GB", "Microsoft Yahei", sans-serif;
```

### segmentfault.com

```
font-family: -apple-system,"Helvetica Neue",Helvetica,Arial,"PingFang SC","Hiragino Sans GB","WenQuanYi Micro Hei","Microsoft Yahei",sans-serif;
```

