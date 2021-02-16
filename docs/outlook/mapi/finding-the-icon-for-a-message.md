---
title: Localizar o ícone de uma mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b351cc68e3c3d9f9c01acb4b3d0e52158e302d7a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409150"
---
# <a name="finding-the-icon-for-a-message"></a>Localizar o ícone de uma mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para encontrar o ícone associado a uma mensagem**
  
1. Chame o método [IMAPIProp::GetProps](imapiprop-getprops.md) da mensagem para recuperar sua **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) .
    
2. Chame [MAPIOpenFormMgr para](mapiopenformmgr.md) recuperar um ponteiro de interface **IMAPIFormMgr.** Passe seu **ponteiro IMAPISession** no parâmetro _pSession._ 
    
3. Chame [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para recuperar um ponteiro da interface **IMAPIFormInfo.** 
    
4. Use o ponteiro **IMAPIFormInfo** para chamar [IMAPIProp::GetProps](imapiprop-getprops.md) e recuperar as propriedades **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) e/ou **PR_MINI_ICON** ([PidTagMiniIcon).](pidtagminiicon-canonical-property.md) 
    

