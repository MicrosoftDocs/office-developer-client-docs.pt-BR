---
title: Estado HandsOffFromNormal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 17fa0f3d4e74ce7d717a94378880f2cc46150fc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299465"
---
# <a name="handsofffromnormal-state"></a>Estado HandsOffFromNormal

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O estado HandsOffFromNormal é muito semelhante ao estado [HandsOffAfterSave](handsoffaftersave-state.md) . Ele faz parte do processo de salvar o conteúdo de um formulário no armazenamento permanente. Quando nesse estado, o objeto Form deve evitar fazer alterações nas cópias na memória dos valores das propriedades da mensagem, porque pode não haver outra oportunidade para salvar essas alterações. A tabela a seguir descreve as transições permitidas do estado HandsOffFromNormal. 
  
|IPersistMessage * * método * *|**Action**|**Novo estado**|
|:-----|:-----|:-----|
|[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) (_PMessage! =_ nulo)  <br/> |Substitua a mensagem do objeto Message por _PMessage_, que é a substituição da mensagem revogada pela chamada anterior a [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md). É garantido que os dados na nova mensagem sejam iguais aos da mensagem revogada. A mensagem não deve ser marcada como limpa, nem [IMAPIViewAdviseSink::](imapiviewadvisesink-onsaved.md) onsaved deve ser chamado após esta chamada. Se a chamada **SaveCompleted** for bem-sucedida, insira o estado [normal](normal-state.md) . Caso contrário, permaneça no estado HandsOffFromNormal.  <br/> |Normal ou HandsOffFromNormal  <br/> |
|**IPersistMessage:: SaveCompleted** (_PMessage = =_ nulo)  <br/> |Defina o último erro como E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|**HandsOffMessage**, [IPersistMessage:: salvar](ipersistmessage-save.md), [IPersistMessage:: InitNew](ipersistmessage-initnew.md)ou [IPersistMessage:: Load](ipersistmessage-load.md) <br/> |Defina o último erro como E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Retorna o último erro.  <br/> |HandsOffFromNormal  <br/> |
|Outros métodos [IPersistMessage: IUnknown](ipersistmessageiunknown.md) de outras interfaces  <br/> |Defina o último erro como E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
   
## <a name="see-also"></a>Confira também



[Estados de formulário](form-states.md)

