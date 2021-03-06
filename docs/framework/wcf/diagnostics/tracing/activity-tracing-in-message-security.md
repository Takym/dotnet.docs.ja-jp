---
title: メッセージ セキュリティにおけるアクティビティ トレース
ms.date: 03/30/2017
ms.assetid: 68862534-3b2e-4270-b097-8121b12a2c97
ms.openlocfilehash: c3bd36598fd903dc016959149e563174624d084b
ms.sourcegitcommit: 296183dbe35077b5c5e5e74d5fbe7f399bc507ee
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/05/2018
ms.locfileid: "50982842"
---
# <a name="activity-tracing-in-message-security"></a>メッセージ セキュリティにおけるアクティビティ トレース
ここでは、次の 3 つの段階で発生するセキュリティ処理のアクティビティ トレースについて説明します。  
  
-   ネゴシエーション/SCT 交換。 トランスポート層 (バイナリデータ交換を使用した場合) またはメッセージ層 (SOAP メッセージ交換を使用した場合) で発生する可能性があります。  
  
-   メッセージの暗号化と復号化、および署名の検証と認証。 トレースは、アンビエント アクティビティ (通常、"プロセス アクション") に表示されます。  
  
-   承認と検証。 ローカルで、またはエンドポイント間の通信中に発生する可能性があります。  
  
## <a name="negotiationsct-exchange"></a>ネゴシエーション/SCT 交換  
 ネゴシエーション/SCT 交換段階では、"セキュリティで保護されたセッションの設定" および "セキュリティで保護されたセッションを閉じる" という 2 種類のアクティビティがクライアント側で作成されます。 "セキュリティで保護されたセッションの設定" は RST/RSTR/SCT メッセージ交換のトレースを含み、"セキュリティで保護されたセッションを閉じる" は "キャンセル" メッセージのトレースを含みます。  
  
 サーバーでは、RST/RSTR/SCT の各要求/応答がそのアクティビティに表示されます。 場合`propagateActivity` = `true`でサーバーとクライアントの両方で、サーバー上でアクティビティ ID は、同じであるし、同時に、セキュリティで保護されたセッションの設定""サービス トレース ビューアーで表示したときに表示されます。  
  
 このアクティビティ トレース モデルは、ユーザー名/パスワード認証、証明書認証、および NTLM 認証に対して有効です。  
  
 ネゴシエーションと SCT 交換のアクティビティとトレースを次の表に示します。  
  
||ネゴシエーション/SCT 交換の発生タイミング|アクティビティ|トレース|  
|-|-------------------------------------------------|----------------|------------|  
|セキュリティで保護されたトランスポート<br /><br /> (HTTPS、SSL)|最初のメッセージを受信したとき。|トレースは、アンビエント アクティビティで出力されます。|交換トレース<br />-セキュリティで保護されたチャネルの確立<br />-共有シークレットの取得します。|  
|セキュリティで保護されたメッセージ層<br /><br /> (WSHTTP)|最初のメッセージを受信したとき。|クライアント側 :<br /><br /> -"セキュリティで保護されたセッションの設定最初のメッセージの「プロセス アクション」帯ごとに RST または RSTR/SCT の要求/応答します。<br />-「閉じるプロキシ アクティビティ」から、交換のキャンセルの「セキュリティで保護されたセッションを閉じる」 このアクティビティは、セキュリティで保護されたセッションが閉じられるタイミングにより、他のアンビエント アクティビティで発生する可能性があります。<br /><br /> サーバー側 :<br /><br /> の各要求/応答の Rst/cancel SCT/サーバー上 1 つの「プロセス アクション」アクティビティ。 場合`propagateActivity` = `true`RST または RSTR//SCT アクティビティは、「セキュリティ セッションの設定」とマージ、および、キャンセル、クライアントからの「閉じる」アクティビティに結合されます。<br /><br /> "セキュリティで保護されたセッションの設定" には 2 つの段階があります。<br /><br /> 1.認証ネゴシエーション。 クライアントが既に適切な資格情報を持つ場合は、省略可能です。 この段階は、セキュリティで保護されたトランスポート、またはメッセージ交換を通じて行われます。 後者の場合、1 つまたは 2 つの RST/RSTR 交換が発生する可能性があります。 これらの交換では、トレースは、従来の設計どおり、新しい要求/応答アクティビティで出力されます。<br />2.セキュリティで保護されたセッションの確立 (SCT)。この段階では、1 つの RST/RSTR 交換が発生します。 前述のように、これには同じアンビエント アクティビティが含まれます。|交換トレース<br />-セキュリティで保護されたチャネルの確立<br />-共有シークレットの取得します。|  
  
> [!NOTE]
>  混在セキュリティ モードでは、ネゴシエーション認証はバイナリ交換で発生しますが、SCT はメッセージ交換で発生します。 純粋なトランスポート モードでは、ネゴシエーションは追加のアクティビティを持たないトランスポートでのみ発生します。  
  
## <a name="message-encryption-and-decryption"></a>メッセージの暗号化と復号化  
 メッセージの暗号化と復号化および署名認証のアクティビティとトレースを次の表に示します。  
  
||セキュリティで保護されたトランスポート<br /><br /> (HTTPS、SSL) およびセキュリティで保護されたメッセージ層 <br /><br /> (WSHTTP)|  
|-|---------------------------------------------------------------------------------|  
|メッセージの暗号化/復号化、および署名認証の発生タイミング|メッセージを受信したとき。|  
|アクティビティ|トレースは、クライアントとサーバーの ProcessAction アクティビティで出力されます。|  
|トレース|-sendSecurityHeader (送信側)。<br />メッセージの署名<br />-要求データを暗号化します。<br />-receiveSecurityHeader (受信側)。<br />-署名を検証します。<br />-応答のデータを復号化します。<br />-認証|  
  
> [!NOTE]
>  純粋なトランスポート モードでは、メッセージの暗号化/復号化は追加のアクティビティを持たないトランスポートでのみ発生します。  
  
## <a name="authorization-and-verification"></a>承認と検証  
 承認のアクティビティとトレースを次の表に示します。  
  
||承認の発生タイミング|アクティビティ|トレース|  
|-|-------------------------------------|----------------|------------|  
|ローカル (既定)|サーバーでメッセージが複号化された後|トレースは、サーバーの ProcessAction アクティビティで出力されます。|ユーザーの承認。|  
|Remote|サーバーでメッセージが複号化された後|トレースは、ProcessAction アクティビティによって呼び出された新しいアクティビティで出力されます。|ユーザーの承認。|
