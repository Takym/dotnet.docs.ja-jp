---
title: アソシエーション セット End
ms.date: 03/30/2017
ms.assetid: fe4bf1d3-047a-4a37-98c5-a66e70811346
ms.openlocfilehash: 440cfdee4581496d9d131fbaf3d1796f38931532
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2018
ms.locfileid: "32756203"
---
# <a name="association-set-end"></a>アソシエーション セット End
*アソシエーション セット end*を識別、[エンティティ型](../../../../docs/framework/data/adonet/entity-type.md)と[エンティティ セット](../../../../docs/framework/data/adonet/entity-set.md)の最後に、[アソシエーション セット](../../../../docs/framework/data/adonet/association-set.md)です。 アソシエーション セット End はアソシエーション セットの一部として定義されます。アソシエーション セットには、アソシエーション セット End が 2 つ必要です。  
  
 アソシエーション セット End の定義には、次の情報が含まれます。  
  
-   アソシエーション セットに含まれるエンティティ型の 1 つ。 (必須)  
  
-   アソシエーション セットに含まれるエンティティ型のエンティティ セット。 (必須)  
  
## <a name="example"></a>例  
 下のダイアグラムは、`WrittenBy` および `PublishedBy` という 2 つのアソシエーションの概念モデルを示しています。  
  
 ![モデルの例](../../../../docs/framework/data/adonet/media/examplemodel.gif "ExampleModel")  
  
 次のダイアグラムには、上の概念モデルに基づくアソシエーション セット (`PublishedBy`) と 2 つのエンティティ セット (`Books` および `Publishers`) を示しています。 アソシエーション セット End は `Books` および `Publishers` エンティティ セットです。 Bi、`Books`エンティティ セットのインスタンスを表し、`Book`実行時にエンティティ型。 同様に、Pj を表す、`Publisher`インスタンス、`Publishers`エンティティ セット。 BiPj がのインスタンスを表し、`PublishedBy`のアソシエーション、`PublishedBy`アソシエーション セット。  
  
 ![例の設定](../../../../docs/framework/data/adonet/media/setsexample.gif "SetsExample")  
  
 [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md)概念スキーマ定義言語と呼ばれる DSL を使用して ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) 概念モデルを定義します。 次の CSDL は、上のダイアグラムの各アソシエーションに対して 1 つのアソシエーション セットを持つエンティティ コンテナーを定義しています。 アソシエーション セット End はアソシエーション セット定義の一部として定義されています。  
  
 [!code-xml[EDM_Example_Model#EntityContainerExample](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books.edmx#entitycontainerexample)]  
  
## <a name="see-also"></a>関連項目  
 [Entity Data Model キーの概念](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)  
 [Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model.md)
