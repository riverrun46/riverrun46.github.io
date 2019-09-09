---
layout: post
title: tailwindcss最佳实践
---

## Tailwind - 定位：设计中的API

### 构建代码时，优先考虑提取公共组件，而不是公共类

对粒度较小的组件，可以考虑使用自建类+@apply提取用到的类。  
对粒度更大的组件（card、modal等），应使用自建组件（html+css）。  
使用laravel-blade / vue-components等工具
  
### 可以考虑不使用sass等pre-processor，只使用PostCSS

```css
@import "tailwindcss/base";
@import "./base.css";

@import "tailwindcss/components";
@import "./components.css";

@import "tailwindcss/utilities";
@import "./utilities.css";
```

### 多使用SVG（icon等）

更方便地使用大小、色彩、不规则形状等

### 勇敢地扩展框架

### 内联样式优于怪异的自定义类

如调整一个多边形的样式尺寸，其值不应该出现在设计系统内，此时使用内联样式更为妥当

### 使用Purgecss清理无用类

___

### 来源

[Tailwind CSS Best Practice Patterns - Adam Wathan on Laracon US 2019](https://youtu.be/J_7_mnFSLDg?list=PL-yJve--iT5qZzp0VzYaPA7ZohLl6tSdp)
