---
title: Localizar o ícone de uma mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b73545585d3279bc290524c7ccb26c14c2977fe4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766541"
---
# <a name="finding-the-icon-for-a-message"></a>Localizar o ícone de uma mensagem

  
  
**Aplica-se a**: Outlook 
  
 **Para localizar o ícone associado a uma mensagem**
  
1. Chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) da mensagem para recuperar sua propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).
    
2. Chame [MAPIOpenFormMgr](mapiopenformmgr.md) para recuperar um ponteiro de interface **IMAPIFormMgr** . Passe o ponteiro **IMAPISession** no parâmetro _pSession_ . 
    
3. Chame [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para recuperar um ponteiro de interface **IMAPIFormInfo** . 
    
4. Use o ponteiro de **IMAPIFormInfo** para chamar [IMAPIProp::GetProps](imapiprop-getprops.md) e recuperar o **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) e/ou propriedades **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). 
    

