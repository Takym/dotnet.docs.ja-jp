---
title: '&lt;オフ&gt;要素&lt;namedCaches&gt;'
ms.date: 03/30/2017
helpviewer_keywords:
- <clear> element for <namedCaches>
- clear element for <namedCaches>
ms.assetid: ea01a858-65da-4348-800f-5e3df59d4d79
author: mcleblanc
ms.author: markl
ms.openlocfilehash: dd521e3afa7584cadb28829028a5ecfd1cb55a92
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2018
ms.locfileid: "53612304"
---
# <a name="ltcleargt-element-for-ltnamedcachesgt"></a>&lt;オフ&gt;要素&lt;namedCaches&gt;
すべてクリア`namedCache`内のエントリ、`namedCaches`メモリ キャッシュのコレクション。  
  
 \<system.runtime.caching>  
\<memoryCache>  
\<namedCaches >  
\<add>  
  
## <a name="syntax"></a>構文  
  
```xml  
<namedCaches>  
    <clear name="default" />  
    <!-- child elements -->  
 </namedCaches>  
```  
  
## <a name="type"></a>型  
 `Type`  
  
## <a name="attributes-and-elements"></a>属性および要素  
 以降のセクションでは、属性、子要素、および親要素について説明します。  
  
### <a name="attributes"></a>属性  
 `None`  
  
### <a name="child-elements"></a>子要素  
 `None`  
  
### <a name="parent-elements"></a>親要素  
  
|要素|説明|  
|-------------|-----------------|  
|[\<namedCaches>](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)|名前付きの構成設定のコレクションを含む<xref:System.Runtime.Caching.MemoryCache>インスタンス。|  
  
## <a name="remarks"></a>Remarks  
 `clear`要素がすべてクリア`namedCache`メモリ キャッシュの名前付きキャッシュのコレクション内のエントリ。 使用することができます、`clear`要素を使用する前に、`add`が他にないを特定するためには新しい名前付きキャッシュ エントリを追加する要素がコレクション内のキャッシュをという名前です。  
  
## <a name="see-also"></a>関連項目  
- [\<namedCaches > 要素 (キャッシュ設定)](../../../../../docs/framework/configure-apps/file-schema/runtime/namedcaches-element-cache-settings.md)
