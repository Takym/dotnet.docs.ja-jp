---
title: '&lt;serviceCredential&gt; の &lt;secureConversationAuthentication&gt;'
ms.date: 03/30/2017
ms.assetid: 0bd3fac7-befd-4a45-ba51-c200b33be0fd
ms.openlocfilehash: 2c8479c4d8a321c822d49bdc24f359ffad5500e9
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54147188"
---
# <a name="ltsecureconversationauthenticationgt-of-ltservicecredentialgt"></a>&lt;serviceCredential&gt; の &lt;secureConversationAuthentication&gt;
安全な会話サービスの設定を指定します。  
  
 \<system.ServiceModel >  
\<<behaviors>  
\<serviceBehaviors>  
\<behavior>  
\<serviceCredentials>  
\<secureConversationAuthentication >  
  
## <a name="syntax"></a>構文  
  
```xml  
<secureConversationAuthentication securityStateEncoderType="String" />
```  
  
## <a name="attributes-and-elements"></a>属性および要素  
 以降のセクションでは、属性、子要素、および親要素について説明します。  
  
### <a name="attributes"></a>属性  
  
|属性|説明|  
|---------------|-----------------|  
|`securityStateEncoderType`|使用される <xref:System.ServiceModel.Security.SecurityStateEncoder> の型を指定する文字列。|  
  
### <a name="child-elements"></a>子要素  
 なし。  
  
### <a name="parent-elements"></a>親要素  
  
|要素|説明|  
|-------------|-----------------|  
|[\<serviceCredentials>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecredentials.md)|サービスの認証に使用される資格情報と、クライアントの資格情報検証関連の設定を指定します。|  
  
## <a name="remarks"></a>Remarks  
 この構成要素を使用して、セキュリティ コンテキスト トークン (SCT) クッキーのシリアル化のための既知のクレームの種類のリストと、クッキーの情報をエンコードしてセキュリティで保護するためのエンコーダーを指定します。 SCT の詳細については、「<xref:System.ServiceModel.Security.SecureConversationServiceCredential>」を参照してください。  
  
## <a name="see-also"></a>関連項目  
 <xref:System.ServiceModel.Configuration.SecureConversationServiceElement>  
 <xref:System.ServiceModel.Configuration.ServiceCredentialsElement.SecureConversationAuthentication%2A>  
 <xref:System.ServiceModel.Description.ServiceCredentials.SecureConversationAuthentication%2A>  
 <xref:System.ServiceModel.Security.SecureConversationServiceCredential>
