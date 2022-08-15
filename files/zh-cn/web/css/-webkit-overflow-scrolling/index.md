---
title: '-webkit-overflow-scrolling'
slug: Web/CSS/-webkit-overflow-scrolling
tags:
  - CSS
  - Non-standard
  - Reference
translation_of: Web/CSS/-webkit-overflow-scrolling
---
<p>{{CSSRef}}{{Non-standard_header}}</p>

<h3 id="概述">概述</h3>

<p><strong><code>-webkit-overflow-scrolling</code></strong> 属性控制元素在移动设备上是否使用滚动回弹效果。</p>

<h3 id="值">值</h3>

<dl>
 <dt><code>auto</code></dt>
 <dd>使用普通滚动，当手指从触摸屏上移开，滚动会立即停止。</dd>
 <dt><code>touch</code></dt>
 <dd>使用具有回弹效果的滚动，当手指从触摸屏上移开，内容会继续保持一段时间的滚动效果。继续滚动的速度和持续的时间和滚动手势的强烈程度成正比。同时也会创建一个新的堆栈上下文。</dd>
</dl>

<h3 id="示例">示例</h3>

<pre class="brush: css">-webkit-overflow-scrolling: touch; /* 当手指从触摸屏上移开，会保持一段时间的滚动 */

-webkit-overflow-scrolling: auto; /* 当手指从触摸屏上移开，滚动会立即停止 */
</pre>

<h3 id="Browser_Compatibility">规范</h3>

<p>尚未有相关规范。另在 Apple 提供的<a href="https://developer.apple.com/library/safari/documentation/AppleApplications/Reference/SafariCSSRef/Articles/StandardCSSProperties.html#//apple_ref/css/property/-webkit-overflow-scrolling">Safari CSS 参考文档</a>中有所提及。</p>

<h3 id="Browser_Compatibility">浏览器兼容性</h3>

{{Compat}}