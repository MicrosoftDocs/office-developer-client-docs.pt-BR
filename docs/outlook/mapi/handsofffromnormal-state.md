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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426468"
---
# <a name="handsofffromnormal-state"></a>Estado HandsOffFromNormal

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O estado HandsOffFromNormal é muito semelhante ao [estado HandsOffAfterSave.](handsoffaftersave-state.md) Ele faz parte do processo de salvar o conteúdo de um formulário em armazenamento permanente. Nesse estado, o objeto de formulário deve evitar fazer alterações nas cópias na memória dos valores das propriedades da mensagem, porque pode não haver outra oportunidade para salvar essas alterações. A tabela a seguir descreve transições permitidas do estado HandsOffFromNormal. 
  
|Método IPersistMessage**|**Ação**|**Novo estado**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)  <br/> |Substitua a mensagem do objeto de mensagem por  _pMessage_, que é a substituição da mensagem revogada pela chamada anterior para [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md). Os dados na nova mensagem são garantidos como os mesmos da mensagem revogada. A mensagem não deve ser marcada como limpa, nem [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) deve ser chamada após essa chamada. Se a **chamada SaveCompleted** for bem-sucedida, insira o [estado Normal.](normal-state.md) Caso contrário, fique no estado HandsOffFromNormal.  <br/> |Normal ou HandsOffFromNormal  <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)  <br/> |De definir o último erro como E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md)ou [IPersistMessage::Load](ipersistmessage-load.md) <br/> |De definir o último erro como E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Retornar o último erro.  <br/> |HandsOffFromNormal  <br/> |
|Outros [IPersistMessage : métodos ou métodos IUnknown](ipersistmessageiunknown.md) de outras interfaces  <br/> |De definir o último erro como E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
   
## <a name="see-also"></a>Confira também



[Estados do formulário](form-states.md)

