---
title: global コンテキスト キーワード - C# リファレンス
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- global
- global_CSharpKeyword
helpviewer_keywords:
- global keyword [C#]
ms.assetid: 8932c16a-6959-42c2-86e7-2c4221ab788b
ms.openlocfilehash: b9273feb38b14dce61facc0f59b0890c431b9a7a
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53240796"
---
# <a name="global-c-reference"></a>global (C# リファレンス)

[:: 演算子](../operators/namespace-alias-qualifer.md)の前に来るとき、`global` コンテキスト キーワードは、C# プログラムの既定の名前空間であるグローバル名前空間を参照し、そうでない場合はグローバル名前空間は付加されません。 詳細については、「[方法 :グローバル名前空間エイリアスを使用する](../../programming-guide/namespaces/how-to-use-the-global-namespace-alias.md)」をご覧ください。

## <a name="example"></a>例

次の例では、コンテキスト キーワード `global` を利用し、グローバル名前空間でクラス `TestApp` が定義されることを指定しています。

[!code-csharp[csrefKeywordsContextual#13](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsContextual/CS/csrefKeywordsContextual.cs#13)]

## <a name="see-also"></a>関連項目

- [名前空間](../../programming-guide/namespaces/index.md)