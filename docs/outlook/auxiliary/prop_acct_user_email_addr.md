---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Especifica o endereço de email da conta.
ms.openlocfilehash: 115941fdf2fdec01da8d6bc1320ac6cdc0930ffa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326527"
---
# <a name="propacctuseremailaddr"></a>PROP_ACCT_USER_EMAIL_ADDR

Especifica o endereço de email da conta.
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x000C  <br/> |
|Tipo de propriedade:  <br/> |PT_UNICODE  <br/> |
|Marca de propriedade:  <br/> |0x000C001F  <br/> |
|Acesso:  <br/> |Leitura/gravação  <br/> |
   
## <a name="remarks"></a>Comentários

 **PROP_ACCT_USER_EMAIL_ADDR** não deve existir em todas as contas. Por exemplo, uma conta do Exchange poderia ter [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) mas não **PROP_ACCT_USER_EMAIL_ADDR**, enquanto for uma conta SMTP/POP3, a situação será revertida.
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de contas](about-the-account-management-api.md)

