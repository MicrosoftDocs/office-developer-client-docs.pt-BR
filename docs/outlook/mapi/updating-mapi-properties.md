---
title: Atualizando propriedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6c2c733b87b85971fad8060040e713b41b0f5616
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407519"
---
# <a name="updating-mapi-properties"></a>Atualizando propriedades MAPI

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os clientes e provedores de serviços podem atualizar um valor de propriedade chamando:
  
- Método [IMAPIProp::SetProps](imapiprop-setprops.md) de um objeto para atualizar o valor de uma ou mais propriedades de um objeto. 
    
- A [função HrSetOneProp](hrsetoneprop.md) para atualizar apenas uma propriedade por vez. Use **HrSetOneProp** somente se o objeto de destino for local; essa função pode causar degradação do desempenho quando usada com objetos remotos. 
    
O procedimento a seguir ilustra como usar **SetProps** para atualizar a classe de mensagem ou PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) de uma mensagem. 
  
### <a name="to-update-the-message-class-of-a-message"></a>Para atualizar a classe de mensagem de uma mensagem 
  
1. Aloce [uma estrutura SPropValue](spropvalue.md) para a classe de mensagem e de definir seus membros conforme apropriado. 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. Chame o método **IMAPIProp::SetProps** da mensagem para definir a nova classe de mensagem. 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a>Confira também

- [Visão geral da propriedade MAPI](mapi-property-overview.md)

