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
ms.openlocfilehash: 512c686a9e5afeadacd8edccedba2c257df48f71
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567808"
---
# <a name="finding-the-icon-for-a-message"></a>Localizar o ícone de uma mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para localizar o ícone associado a uma mensagem**
  
1. Chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) da mensagem para recuperar sua propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).
    
2. Chame [MAPIOpenFormMgr](mapiopenformmgr.md) para recuperar um ponteiro de interface **IMAPIFormMgr** . Passe o ponteiro **IMAPISession** no parâmetro _pSession_ . 
    
3. Chame [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para recuperar um ponteiro de interface **IMAPIFormInfo** . 
    
4. Use o ponteiro de **IMAPIFormInfo** para chamar [IMAPIProp::GetProps](imapiprop-getprops.md) e recuperar o **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) e/ou propriedades **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). 
    

