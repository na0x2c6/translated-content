---
title: CSSStyleDeclaration.parentRule
slug: Web/API/CSSStyleDeclaration/parentRule
tags:
- API
- CSSOM
- Property
- Reference
browser-compat: api.CSSStyleDeclaration.parentRule
translation_of: Web/API/CSSStyleDeclaration/parentRule
---
<p>{{ APIRef("CSSOM") }}</p>

<p><span class="seoSummary"><strong>CSSStyleDeclaration.parentRule</strong> は読み取り専用のプロパティで、このスタイルブロックの親である {{domxref('CSSRule')}} を返します。</span>例えば、 CSS セレクターのスタイルを表す {{domxref('CSSStyleRule')}} です。</p>

<h2 id="Syntax">構文</h2>

<pre class="brush: js">var <em>rule</em> = <em>styles</em>.parentRule;</pre>

<h3 id="Value">値</h3>

<p>この宣言ブロックを含む CSS 規則、またはこの {{domxref('CSSStyleDeclaration')}} が {{domxref('CSSRule')}} に割り当てられていない場合は <code>null</code> を返します。</p>

<h2 id="Example">例</h2>

<p>次の JavaScript コードは、 {{domxref('CSSStyleDeclaration')}} から親の CSS スタイル規則を取得します。</p>

<pre class="brush: js">var declaration = document.styleSheets[0].rules[0].style;
var rule = declaration.parentRule;
</pre>

<h2 id="Specifications">仕様書</h2>

{{Specifications}}

<h2 id="Browser_compatibility">ブラウザーの互換性</h2>

<p>{{Compat}}</p>