---
title: ::演算子 - C# リファレンス
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ::_CSharpKeyword
helpviewer_keywords:
- ':: operator [C#]'
- 'namespaces [C#], :: operator'
- namespace alias qualifier operator (::) [C#]
ms.assetid: 698b5a73-85cf-4e0e-9e8e-6496887f8527
ms.openlocfilehash: 2e456be075f3487676228244e0119ff46ed9a538
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53243479"
---
# <a name="-operator-c-reference"></a>::演算子 (C# リファレンス)
名前空間エイリアス修飾子 (`::`) を使用して識別子を検索できます。 この例に示すように、常に 2 つの識別子の間に配置します。  
  
 [!code-csharp[csRefOperators#27](../../../csharp/language-reference/operators/codesnippet/CSharp/namespace-alias-qualifer_1.cs)]  

`::` 演算子は、"*using 別名ディレクティブ*" と一緒に使用することもできます。

```csharp
// using Col=System.Collections.Generic;
var numbers = new Col::List<int> { 1, 2, 3 };
```

## <a name="remarks"></a>コメント  
 名前空間エイリアス修飾子として `global` を指定できます。 これにより、エイリアスを使用した名前空間ではなく、グローバル名前空間で検索が実行されます。  
  
## <a name="for-more-information"></a>参照項目  
 `::` 演算子の使用例については、次のセクションを参照してください。  
  
-   [方法: グローバル名前空間エイリアスを使用する](../../../csharp/programming-guide/namespaces/how-to-use-the-global-namespace-alias.md)  
  
## <a name="c-language-specification"></a>C# 言語仕様  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>参照

- [C# リファレンス](../../../csharp/language-reference/index.md)  
- [C# プログラミングガイド](../../../csharp/programming-guide/index.md)  
- [C# 演算子](../../../csharp/language-reference/operators/index.md)  
- [名前空間キーワード](../../../csharp/language-reference/keywords/namespace-keywords.md)  
- [.演算子](../../../csharp/language-reference/operators/member-access-operator.md)  
- [extern エイリアス](../../../csharp/language-reference/keywords/extern-alias.md)
