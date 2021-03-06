---
title: when - C# リファレンス
ms.custom: seodec18
ms.date: 03/07/2017
f1_keywords:
- when_CSharpKeyword
- when
helpviewer_keywords:
- when keyword [C#]
ms.assetid: dd543335-ae37-48ac-9560-bd5f047b9aea
ms.openlocfilehash: 103309b5e5a121647576ce120f4353b4ceef08c4
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53235528"
---
 # <a name="when-c-reference"></a>when (C# リファレンス)

コンテキスト キーワード `when` は、次の 2 つのコンテキストでフィルター条件を指定するために使用できます。

- [try/catch](try-catch.md) または [try/catch/finally](try-catch-finally.md) ブロックの `catch` ステートメント。
- [switch](switch.md) ステートメントの `case` ラベル。

## <a name="when-in-a-catch-statement"></a>`catch` ステートメントでの `when`

C# 6 から、`when` を `catch` ステートメントで使用して、特定の例外のハンドラーを実行するために true になる必要がある条件を指定できるようになりました。 構文は次のとおりです。

```csharp
catch (ExceptionType [e]) when (expr)
```
*expr* の箇所には、ブール値に評価される式を指定します。 `true` が返された場合は、例外ハンドラーが実行されます。`false` の場合は実行されません。 

次の例では、`when` キーワードを使用し、例外メッセージのテキストに応じて、<xref:System.Net.Http.HttpRequestException> のハンドラーが条件付きで実行されるようにしています。

 [!code-csharp[when-with-catch](../../../../samples/snippets/csharp/language-reference/keywords/when/catch.cs)]  
  
## <a name="when-in-a-switch-statement"></a>`switch` ステートメントでの `when`

C# 7.0 以降では、`case` ラベルが相互に排他的である必要がなくなり、`switch` ステートメントでの `case` ラベルの表示順序によって、実行される switch ブロックを決定できるようになりました。 `when` キーワードを使用すると、フィルター条件が true である場合にのみ、関連付けられた case ラベルも true になるフィルター条件を指定できます。 構文は次のとおりです。

```csharp
case (expr) when (when-condition):
```
*expr* の箇所には、match 式と比較される定数パターンまたは型パターンを指定し、*when-condition* の箇所には、任意のブール式を指定します。 

次の例では、`when` キーワードを使用して、面積が 0 の `Shape` オブジェクトに対するテストと、面積が 0 より大きい各種の `Shape` オブジェクトに対するテストを実行しています。 

 [!code-csharp[when-with-case#1](../../../../samples/snippets/csharp/language-reference/keywords/when/when.cs#1)]  

## <a name="see-also"></a>関連項目

- [switch ステートメント](switch.md)  
- [try/catch ステートメント](try-catch.md)  
- [try/catch/finally ステートメント](try-catch-finally.md) 
