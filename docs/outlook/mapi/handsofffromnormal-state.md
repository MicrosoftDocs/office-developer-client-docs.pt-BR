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
ms.openlocfilehash: 92c604c621e2837b76e9e49fd182524ad17fbcac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588339"
---
# <a name="handsofffromnormal-state"></a>Estado HandsOffFromNormal

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O estado de HandsOffFromNormal é muito similar ao estado [HandsOffAfterSave](handsoffaftersave-state.md) . Ele faz parte do processo de salvar o conteúdo de um formulário em um armazenamento permanente. Quando nesse estado, o objeto form deve Evite as alterações as cópias na memória dos valores das propriedades da mensagem, pois não pode ser outra oportunidade salvar estas alterações. A tabela a seguir descreve as transições permitidas do estado de HandsOffFromNormal. 
  
|IPersistMessage * * método * *|**Action**|**Novo estado**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ nulo)  <br/> |Substitua mensagem do objeto mensagem _pMessage_, que é a substituição da mensagem revogado pela chamada anterior à [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md). São garantidos que os dados na nova mensagem ser os mesmos que a mensagem revogada. A mensagem não deve ser marcada como limpar, nem [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) deve ser chamado após essa chamada. Se a chamada **SaveCompleted** tiver êxito, insira o estado [Normal](normal-state.md) . Caso contrário, mantenha-se no estado HandsOffFromNormal.  <br/> |Normal ou HandsOffFromNormal  <br/> |
|**IPersistMessage::SaveCompleted** (_pMessage = =_ nulo)  <br/> |Defina o último erro como E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md)ou [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Defina o último erro como E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Retorna o último erro.  <br/> |HandsOffFromNormal  <br/> |
|Outros [IPersistMessage: IUnknown](ipersistmessageiunknown.md) métodos ou métodos de outras interfaces  <br/> |Defina o último erro como E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
   
## <a name="see-also"></a>Confira também



[Estados de formulários](form-states.md)

