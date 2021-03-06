---
title: '&lt;clientCredentials&gt; 要素の &lt;clientCertificate&gt;'
ms.date: 03/30/2017
ms.assetid: 3b3fa000-3434-4142-a178-11903bdd2c5d
ms.openlocfilehash: f6dbc2c7d43558d86f74468adbc7026e8462812c
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2019
ms.locfileid: "54147942"
---
# <a name="ltclientcertificategt-of-ltclientcredentialsgt-element"></a>&lt;clientCredentials&gt; 要素の &lt;clientCertificate&gt;
サービスに対するクライアントの認証に使用する X.509 証明書を定義します。  
  
 \<system.ServiceModel >  
\<<behaviors>  
\<endpointBehaviors>  
\<behavior>  
\<clientCredentials>  
\<clientCertificate >  
  
## <a name="syntax"></a>構文  
  
```xml  
<clientCertificate findValue="String"
                   storeLocation="LocalMachine/CurrentUser"
                   storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"
                   X509FindType="FindByThumbPrint/FindBySubjectName/FindBySubjectDistinguishedName/FindByIssuerName/FindByIssuerDistinguishedName/FindBySerialNumber/FindByTimeValid/FindByTimeNotYetValid/FindByTemplateName/FindByApplicationPolicy/FindByCertificatePolicy/FindByExtension/FindByKeyUsage/FindBySubjectKeyIdentifier" />
```  
  
## <a name="attributes-and-elements"></a>属性および要素  
 以降のセクションでは、属性、子要素、および親要素について説明します。  
  
### <a name="attributes"></a>属性  
  
|属性|説明|  
|---------------|-----------------|  
|`findValue`|X.509 証明書ストアで検索する値を含む文字列。 属性に格納されている型は、`X509FindType` 属性値の要件を満たす必要があります。 既定値は空の文字列です。|  
|`storeLocation`|クライアントがサービスに対して自身を認証するために使用する X.509 証明書の場所を指定します。 以下の値が有効です。<br /><br /> -LocalMachine: ローカル マシンに割り当てられている証明書ストア。<br />-CurrentUser: 現在のユーザーに割り当てられている証明書ストア。<br /><br /> 既定は LocalMachine です。 この属性は <xref:System.Security.Cryptography.X509Certificates.StoreLocation> 型です。|  
|`storeName`|検索する X.509 証明書ストアの名前を指定します。 以下の値が有効です。<br /><br /> -AddressBook:他のユーザーの証明書ストア。<br />-AuthRoot:サード パーティ証明機関 (Ca) 証明書ストア。<br />-[証明機関]:中間証明機関 (Ca) 証明書ストア。<br />-許可されていません。失効した証明書の証明書ストア。<br />-My:個人用証明書の証明書ストア。<br />ルート:信頼されたルート証明機関 (Ca) 証明書ストア。<br />-TrustedPeople:直接信頼されたユーザーとリソースの証明書ストア。<br />-TrustedPublisher:直接信頼された発行者の証明書ストア。<br /><br /> 既定値は My です。 この属性は <xref:System.Security.Cryptography.X509Certificates.StoreName> 型です。|  
|X509FindType|実行する X.509 検索の種類を定義します。 `findValue` 属性に格納されている型は、この属性の要件を満たす必要があります。 以下の値が有効です。<br /><br /> -FindByThumbPrint<br />-   FindBySubjectName<br />-FindBySubjectDistinguishedName<br />-   FindByIssuerName<br />-FindByIssuerDistinguishedName<br />-   FindBySerialNumber<br />-   FindByTimeValid<br />-   FindByTimeNotYetValid<br />-   FindByTemplateName<br />-   FindByApplicationPolicy<br />-FindByCertificatePolicy<br />-FindByExtension<br />-   FindByKeyUsage<br />-   FindBySubjectKeyIdentifier<br /><br /> 既定値は FindBySubjectDistinguishedName です。 この属性は <xref:System.Security.Cryptography.X509Certificates.X509FindType> 型です。|  
  
### <a name="child-elements"></a>子要素  
 なし。  
  
### <a name="parent-elements"></a>親要素  
  
|要素|説明|  
|-------------|-----------------|  
|[\<clientCredentials>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md)|サービスに対するクライアントの認証に使用される資格情報を指定します。|  
  
## <a name="remarks"></a>Remarks  
 この構成要素は、この要素によるクライアントの認証に使用する証明書を指定します。 詳細については、「[方法 :クライアント資格情報の値を指定](../../../../../docs/framework/wcf/how-to-specify-client-credential-values.md)します。  
  
## <a name="see-also"></a>関連項目  
 <xref:System.ServiceModel.Configuration.ClientCredentialsElement>  
 <xref:System.ServiceModel.Configuration.ClientCredentialsElement.ClientCertificate%2A>  
 <xref:System.ServiceModel.Description.ClientCredentials>  
 <xref:System.ServiceModel.Description.ClientCredentials.ClientCertificate%2A>  
 <xref:System.ServiceModel.Configuration.X509InitiatorCertificateServiceElement>  
 <xref:System.ServiceModel.Security.X509CertificateInitiatorClientCredential>  
 [セキュリティ動作](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)  
 [方法: クライアント資格情報の値を指定します。](../../../../../docs/framework/wcf/how-to-specify-client-credential-values.md)  
 [クライアントのセキュリティ保護](../../../../../docs/framework/wcf/securing-clients.md)  
 [証明書の使用](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)  
 [サービスおよびクライアントのセキュリティ保護](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
