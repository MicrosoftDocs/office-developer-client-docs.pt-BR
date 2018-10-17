---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: Recupera ou define a ID de entrada do catálogo de endereços da conta.
ms.openlocfilehash: 2352f64b46e9884e95b7bf1f3693321f7cd224ca
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400342"
---
# <a name="propmapiidentityentryid"></a>PROP_MAPI_IDENTITY_ENTRYID

Recupera ou define a ID de entrada do catálogo de endereços da conta.
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x2002  <br/> |
|Tipo de propriedade:  <br/> |PT_BINARY  <br/> |
|Marca de propriedade:  <br/> |0x20020102  <br/> |
|Acesso:  <br/> |Leitura/gravação  <br/> |
   
## <a name="remarks"></a>Comentários

 **PROP\_MAPI\_IDENTITY\_ENTRYID** não precisa existir em toda conta. Por exemplo, uma conta do Exchange pode ter **PROP\_MAPI\_IDENTITY\_ENTRYID** definidos, e não [PROP\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), enquanto para uma conta POP3/SMTP a situação é reversa. **PROP\_MAPI_IDENTITY_ENTRYID** retorna uma ID de entrada semelhante ao valor retornado por _lppEntryID_ em [IMAPISession::QueryIdentity](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx). 
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de contas](about-the-account-management-api.md)

