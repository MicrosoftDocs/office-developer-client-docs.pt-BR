---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: Obtém ou define a identificação de entrada do catálogo de endereços para a conta.
ms.openlocfilehash: d85a779da36c2780fe058f906086f61cfc47d5d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766060"
---
# <a name="propmapiidentityentryid"></a>PROP_MAPI_IDENTITY_ENTRYID

Obtém ou define a identificação de entrada do catálogo de endereços para a conta.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x2002  <br/> |
|Tipo de propriedade:  <br/> |PT_BINARY  <br/> |
|Marca de propriedade:  <br/> |0x20020102  <br/> |
|Access:  <br/> |Leitura/gravação  <br/> |
   
## <a name="remarks"></a>Coment�rios

 **PROP\_MAPI\_identidade\_ENTRYID** não deve existir em cada conta. Por exemplo, uma conta do Exchange poderia ter **PROP\_MAPI\_identidade\_ENTRYID** definido e não [PROP\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md)enquanto revertida para uma conta de SMTP/POP3 a situação. **PROP\_MAPI_IDENTITY_ENTRYID** retorna uma identificação de entrada é semelhante ao valor retornado pela _lppEntryID_ em [IMAPISession::QueryIdentity](http://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx). 
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de conta](about-the-account-management-api.md)

