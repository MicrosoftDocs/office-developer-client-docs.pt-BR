---
title: Atualizando propriedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 172abe64073b11d98bfb5f76999237218ef8944a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581346"
---
# <a name="updating-mapi-properties"></a>Atualizando propriedades MAPI

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Clientes e provedores de serviços podem atualizar um valor de propriedade chamando:
  
- Um método do objeto [IMAPIProp::SetProps](imapiprop-setprops.md) para atualizar o valor de uma ou mais das propriedades de um objeto. 
    
- A função [HrSetOneProp](hrsetoneprop.md) para atualizar a propriedade de apenas um por vez. Use **HrSetOneProp** somente se o objeto de destino é local; Esta função pode causar degradação do desempenho quando usado com objetos remotos. 
    
O procedimento a seguir ilustra como usar **SetProps** para atualizar a classe de mensagem ou a propriedade PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), de uma mensagem. 
  
### <a name="to-update-the-message-class-of-a-message"></a>Para atualizar a classe de mensagem de uma mensagem 
  
1. Alocar uma estrutura de [SPropValue](spropvalue.md) para a classe de mensagem e definir seus membros conforme apropriado. 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. Chame o método de **IMAPIProp::SetProps** da mensagem para definir a nova classe de mensagem. 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a>Confira também

- [Visão geral da propriedade MAPI](mapi-property-overview.md)

