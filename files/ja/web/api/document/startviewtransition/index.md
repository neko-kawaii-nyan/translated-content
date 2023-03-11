---
title: Document.startViewTransition()
slug: Web/API/Document/startViewTransition
page-type: web-api-instance-method
l10n:
  sourceCommit: 1715a2acd75550d9e75e29154ca5d05147be8dd3
---

{{APIRef("Document")}}{{SeeCompatTable}}

{{domxref("View Transitions API", "View Transitions API", "", "nocode")}} の **`startViewTransition()`** メソッドは、ビュー遷移を開始し、開始した遷移を表す {{domxref("ViewTransition")}} オブジェクトを返します。

`startViewTransition()` が呼び出されたときの処理順は、[ビュー遷移の過程](/ja/docs/Web/API/View_Transitions_API#ビュー遷移の過程) を参照してください。

## 構文

```js-nolint
startViewTransition(callback)
```

### 引数

- `callback`
  - : Promise を返すコールバック関数です。ビュー遷移処理中にDOMを更新するために呼び出されます。コールバック関数は、API が現在のページのスクリーンショットを取得した時点で呼び出されます。コールバック関数が返した Promise の処理が完了すると、次のフレームでビューの遷移が開始されます。Promise の処理が失敗した場合は、ビューの遷移は中断されます。

### 返値

{{domxref("ViewTransition")}} オブジェクトのインスタンス。

## 例

### 基本的な使い方

[View Transitions の簡単なデモ](https://mdn.github.io/dom-examples/view-transitions/)では、`updateView()` 関数は View Transitions API をサポートしているブラウザーとサポートしていないブラウザーの両方に対応しています。サポートしているブラウザーでは、`startViewTransition()` を呼び出すことで、返値を気にかけることなく、ビューの遷移処理を開始させています。

```js
function updateView(event) {
  // <a> と <img> のどちらでイベントが発火されたかによって処理を分ける
  let targetIdentifier;
  if (event.target.firstChild === null) {
    targetIdentifier = event.target;
  } else {
    targetIdentifier = event.target.firstChild;
  }

  const displayNewImage = () => {
    const mainSrc = `${targetIdentifier.src.split("_th.jpg")[0]}.jpg`;
    galleryImg.src = mainSrc;
    galleryCaption.textContent = targetIdentifier.alt;
  };

  // View Transitions がサポートされていないブラウザー用の実装
  if (!document.startViewTransition) {
    displayNewImage();
    return;
  }

  // View Transitions での実装
  const transition = document.startViewTransition(() => displayNewImage());
}
```

## 仕様書

{{Specifications}}

## ブラウザーの互換性

{{Compat}}

## 関連情報

- [Smooth and simple transitions with the View Transitions API](https://developer.chrome.com/docs/web-platform/view-transitions/)
