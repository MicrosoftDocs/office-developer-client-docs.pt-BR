---
title: Estado HandsOffAfterSave
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 274e7206171e1874e3625896952f861d25f3b382
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564532"
---
# <a name="handsoffaftersave-state"></a>Estado HandsOffAfterSave

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O estado de HandsOffAfterSave faz parte do processo de salvar o conteúdo de um formulário em um armazenamento permanente. Quando nesse estado, o objeto form deve Evite as alterações as cópias na memória dos valores das propriedades da mensagem, pois não pode ser outra oportunidade salvar estas alterações. A tabela a seguir descreve as transições permitidas do estado de HandsOffAfterSave.
  
|**Método IPersistMessage**|**Action**|**Novo estado**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ nulo)  <br/> |Abra quaisquer objetos incorporados. Os dados na mensagem armazenado em _pMessage_ são garantidos para ser o mesmo que a mensagem na chamada [IPersistMessage::Save](ipersistmessage-save.md) anterior. Se a chamada **SaveCompleted** tiver êxito, insira o estado Normal. Caso contrário, defina o último erro para E_OUTOFMEMORY e permanecer no estado HandsOffAfterSave.  <br/> |[Normal](normal-state.md) ou HandsOffAfterSave  <br/> |
|**IPersistMessage::SaveCompleted** (_pMessage = =_ nulo)  <br/> |Defina o último erro E_INVALIDARG ou E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Salvar**ou [IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Defina o último erro como e retornar E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Carregar o objeto de formulário com os dados da mensagem de destino. Essa chamada pode ocorrer quando o objeto de formulário será a mensagem anterior ou seguinte em uma pasta.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Retorna o último erro.  <br/> |HandsOffAfterSave  <br/> |
|Outros [IPersistMessage: IUnknown](ipersistmessageiunknown.md) métodos ou métodos de outras interfaces  <br/> |Defina o último erro como e retornar E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
   
## <a name="see-also"></a>Confira também



[Estados de formulários](form-states.md)

