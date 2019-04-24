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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336950"
---
# <a name="finding-the-icon-for-a-message"></a>Localizar o ícone de uma mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para localizar o ícone associado a uma mensagem**
  
1. Chame o método [IMAPIProp::](imapiprop-getprops.md) GetProps da mensagem para recuperar sua propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).
    
2. Chame [MAPIOpenFormMgr](mapiopenformmgr.md) para recuperar um ponteiro de interface **IMAPIFormMgr** . Passe o ponteiro do **IMAPISession** no parâmetro _pSession_ . 
    
3. Chame [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para recuperar um ponteiro de interface do **IMAPIFormInfo** . 
    
4. Use o **ponteiro IMAPIFormInfo** para chamar [IMAPIProp::](imapiprop-getprops.md) GetProps e recuperar as propriedades **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) e/ou **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). 
    

