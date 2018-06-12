---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Especifica o endereço de email para a conta.
ms.openlocfilehash: 7d0bbba2dcb104326c360da6a10f3e19d1740e46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766063"
---
# <a name="propacctuseremailaddr"></a>PROP_ACCT_USER_EMAIL_ADDR

Especifica o endereço de email para a conta.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x000C  <br/> |
|Tipo de propriedade:  <br/> |PT_UNICODE  <br/> |
|Marca de propriedade:  <br/> |0x000C001F  <br/> |
|Access:  <br/> |Leitura/gravação  <br/> |
   
## <a name="remarks"></a>Coment�rios

 Espera- **PROP_ACCT_USER_EMAIL_ADDR** não existir em cada conta. Por exemplo, uma conta do Exchange poderia ter [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) , mas não **PROP_ACCT_USER_EMAIL_ADDR**, enquanto que para uma conta de SMTP/POP3, a situação é inversa.
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de conta](about-the-account-management-api.md)

