---
title: 'ARIA: img ロール'
slug: orphaned/Web/Accessibility/ARIA/Roles/Role_Img
tags:
  - ARIA
  - ARIA Role
  - Accessibility
translation_of: Web/Accessibility/ARIA/Roles/Role_Img
original_slug: Web/Accessibility/ARIA/Roles/Role_Img
---
ARIA の画像 (`img`) ロールは、単一の画像とみなすべきページコンテンツ内の複数の要素を識別するために使用できます。 これらの要素は、組み合わせることで視覚的な方法で情報を伝達できる、画像、コードスニペット、テキスト、絵文字、またはその他のコンテンツである可能性があります。

```html
<div role="img" aria-label="全体的な画像の説明">
  <img src="graphic1.png" alt="">
  <img src="graphic2.png">
</div>
```

## 説明

単一の画像として消費されるべきコンテンツの集合 (画像、動画、音声、コードスニペット、絵文字、その他のコンテンツを含む) は、画像ロール (`role="img"`) を使用して識別できます。

支援技術にコンテキストを伝えるために、個々の画像要素の代替テキストを当てにするべきではありません。 ほとんどのスクリーンリーダーは、画像ロール (`role="img"`) を持つ要素をブラックボックスのように見なし、内部の個々の要素にはアクセスしません。 したがって、周囲のテキストの中か、`aria-label` 属性を使用して、画像の包括的で全体的な説明の代替テキストを提供します。 また、画像が失敗した場合に、検索エンジンまたはサイトユーザーがページに書き込めるように、任意で `alt` 属性を提供します。

```html
<div role="img" aria-label="全体的な画像の説明">
  <img src="graphic1.png" alt="">
  <img src="graphic2.png">
</div>
```

画像にページに表示されるキャプションやラベルを追加したい場合は、次の方法を使用できます。

- テキストが簡潔なラベルの場合は、`aria-labelledby`。
- テキストがより長い説明である場合は、`aria-describedby`。

例えば、

```html
<div role="img" aria-labelledby="image-1">
  ...
  <p id="image-1">画像のグループを説明するテキスト。</p>
</div>
```

### SVG と role="img"

ページ内で埋め込み SVG 画像を使用している場合は、外側の `<svg>` 要素に画像ロール (`role="img"`) を設定し、ラベルを付けることをお勧めします。 これにより、スクリーンリーダーは、この要素を単一の実体とみなし、全ての子ノードを読み上げようとするのではなく、ラベルを使用して説明するようになります。

```html
<svg role="img" aria-label="SVG 画像の説明">
  <!-- SVG 画像の内容 -->
</svg>
```

### role="img" を使用して、不明瞭や暗黙なものに意味を付与する

場合によっては、支援技術のユーザーは、特定の方法で表現されたり、特定の媒体を通したり、特定の方法で暗示されたコンテンツの意味を理解することができません。 これは画像の場合は明らかに直せますが (`alt` 属性を使うことができます) 、混在したコンテンツや他の特定の種類のコンテンツの場合はそれほど明白ではないので、画像ロール (`role="img"`) が有用になります。

例えば、テキストに絵文字を使用した場合、その意味は目の見えるユーザーにとっては明白かもしれませんが、スクリーンリーダーを使用している人は、絵文字にはテキスト表現が全くないか、代替テキストが紛らわしく、それが使用されているコンテキストと一致しないために混乱する可能性があります。 例えば、次のコードです。

```html
<div role="img" aria-label="その猫はとても面白い">
  <p>
    &#x1F408; &#x1F602;
  </p>
</div>
```

\&#x1F408; \&#x1F602; の絵文字の実体参照は「猫」と「涙が出るほど嬉しい顔」で読み上げられますが、これは必ずしも意味をなしません — 暗黙の意味はおそらく「その猫はとても面白い」で、それを `aria-label` で画像ロール (`role="img"`) と一緒に指定します。

これは、いくつかのブラウザーとスクリーンリーダーの組み合わせでは問題なく動作するようですが、中にはラベルを 2 回読み上げてしまうものもあります。 注意して使用し、徹底的にテストしてください。

これが適している別の例は、伝説的な「ちゃぶ台返し」のような ASCII 絵文字の組み合わせを使用する場合です。

```html
<div role="img" aria-label="ちゃぶ台返し">
  <p>
    (╯°□°）╯︵ ┻━┻
  </p>
</div>
```

### 関連する WAI-ARIA のロール、ステート、プロパティ

- aria-label
  - : アクセス可能な名前が必要です。 aria-label 属性

### キーボードインタラクション

### 必要な JavaScript 機能

## 例

- [星評価 role="img"の例](https://codepen.io/svinkle/pen/oYjoNE)

## 仕様

| 仕様                                         | 状態                     |
| -------------------------------------------- | ------------------------ |
| {{SpecName("ARIA","#img","img")}} | {{Spec2('ARIA')}} |

## スクリーンリーダーのサポート

TBD

## 関連情報

- [Accessibility Object Model](https://wicg.github.io/aom/spec/)
- [ARIA in HTML](https://w3c.github.io/html-aria/)

1.  [**WAI-ARIA ロール**](/ja/docs/Web/Accessibility/ARIA/Roles){{ListSubpagesForSidebar("/ja/docs/Web/Accessibility/ARIA/Roles")}}
