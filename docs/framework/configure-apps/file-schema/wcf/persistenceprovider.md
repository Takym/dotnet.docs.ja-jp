---
title: '&lt;persistenceProvider&gt;'
ms.date: 03/30/2017
ms.assetid: a37049c5-a7ea-4519-94f2-912eeb010380
ms.openlocfilehash: ba02977a7df44931ae195040949e9a8eb0c141b5
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54152022"
---
# <a name="ltpersistenceprovidergt"></a>&lt;persistenceProvider&gt;
使用する永続化プロバイダーの実装の型と、永続化操作に使用するタイムアウトを指定します。  
  
 \<system.ServiceModel >  
\<<behaviors>  
\<serviceBehaviors>  
\<behavior>  
\<persistenceProvider >  
  
## <a name="syntax"></a>構文  
  
```xml  
<persistenceProvider persistenceOperationTimeout="TimeSpan"
                     type="String" />
```  
  
## <a name="attributes-and-elements"></a>属性および要素  
 以降のセクションでは、属性、子要素、および親要素について説明します。  
  
### <a name="attributes"></a>属性  
  
|属性|説明|  
|---------------|-----------------|  
|persistenceOperationTimeout|永続化動作に使用するタイムアウトを指定する <xref:System.TimeSpan> 値。 既定値は"00: 00:30"。|  
|型|使用する永続化プロバイダー ファクトリの型を指定する文字列。|  
  
### <a name="child-elements"></a>子要素  
 なし。  
  
### <a name="parent-elements"></a>親要素  
  
|要素|説明|  
|-------------|-----------------|  
|[\<behavior>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|動作の要素を指定します。|  
  
## <a name="remarks"></a>Remarks  
 この要素は、WCF サービスの状態をシリアル化するために使用される永続化プロバイダーを指定します。 HTTP ヘッダーに状態情報を渡す `wsHttpContextBinding` と一緒に使用する必要があります。  
  
## <a name="see-also"></a>関連項目  
 <xref:System.ServiceModel.Configuration.PersistenceProviderElement>  
 <xref:System.ServiceModel.Persistence.PersistenceProvider>
