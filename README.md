#YJChineseSorting

## iOS通讯录联系人列表(中文排序)
![First Image](/Users/God/Desktop/YJChineseSorting/sample.gif "First Image")

### 一、导入头文件#import <ChineseString.h>
### 二、数据源
1.cell显示数据
```
NSArray *stringsToSort = [NSArray arrayWithObjects:
                              @"杨京",@"王传玉",@"开源中国 ",@"王建中",
                              @"开源技术",@"社区",@"开发者",@"传播",
                              @"2014",@"a1",@"100",@"中国",@"暑假作业",
                              @"键盘", @"鼠标",@"hello",@"world",@"b1",
                              nil];
```
2.点击cell显示数据
```
    NSArray *NumberToSort = [NSArray arrayWithObjects:
                             @"杨京0023",@"王传玉0024",@"开源中国0025 ",@"王建中0026",
                             @"开源技术0027",@"社区0028",@"开发者0029",@"传播0010",
                             @"2014",@"a1",@"100",@"中国",@"暑假作业",
                             @"键盘", @"鼠标",@"hello",@"world",@"b1",
                             nil];
```
### 三、注意
因为中文排序里面有c的文件 pinyin.c

plan 1：

pch文件如下 例如：

  #ifdef __OBJC__
  
  #import "AppDelegate.h"
  
  #endif

  __OBJC__表示宏内引用的文件确保只被使用Objective-C语言的文件所引用，保证引用关系的清晰。
  
plan 2 ：

pinyin.c 改为pinyin.m
