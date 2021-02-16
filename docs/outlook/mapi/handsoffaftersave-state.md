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
ms.openlocfilehash: 85630965c7e78e6fa76e348bfe98cc9060665057
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406602"
---
# <a name="handsoffaftersave-state"></a>Estado HandsOffAfterSave

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O estado HandsOffAfterSave faz parte do processo de salvar o conteúdo de um formulário em armazenamento permanente. Nesse estado, o objeto de formulário deve evitar fazer alterações nas cópias na memória dos valores das propriedades da mensagem, porque pode não haver outra oportunidade para salvar essas alterações. A tabela a seguir descreve transições permitidas do estado HandsOffAfterSave.
  
|**Método IPersistMessage**|**Ação**|**Novo estado**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)  <br/> |Abra todos os objetos incorporados. Os dados na mensagem armazenada em  _pMessage_ são garantidos como os mesmos da mensagem na chamada [IPersistMessage::Save](ipersistmessage-save.md) anterior. Se a **chamada SaveCompleted** for bem-sucedida, insira o estado Normal. Caso contrário, de definida a última E_OUTOFMEMORY e fique no estado HandsOffAfterSave.  <br/> |[Normal](normal-state.md) ou HandsOffAfterSave  <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)  <br/> |De definir o último erro como E_INVALIDARG ou E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save** ou [IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |De definida a última mensagem de erro e retorne E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Carregue o objeto de formulário com dados da mensagem de destino. Essa chamada pode ocorrer quando o objeto de formulário está indo para a mensagem seguinte ou anterior em uma pasta.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Retornar o último erro.  <br/> |HandsOffAfterSave  <br/> |
|Outros [IPersistMessage : métodos ou métodos IUnknown](ipersistmessageiunknown.md) de outras interfaces  <br/> |De definida a última mensagem de erro e retorne E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
   
## <a name="see-also"></a>Confira também



[Estados do formulário](form-states.md)

