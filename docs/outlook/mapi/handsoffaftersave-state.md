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
  
O estado HandsOffAfterSave é parte do processo de salvar o conteúdo de um formulário no armazenamento permanente. Quando nesse estado, o objeto Form deve evitar fazer alterações nas cópias na memória dos valores das propriedades da mensagem, porque pode não haver outra oportunidade para salvar essas alterações. A tabela a seguir descreve as transições permitidas do estado HandsOffAfterSave.
  
|**Método IPersistMessage**|**Action**|**Novo estado**|
|:-----|:-----|:-----|
|[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) (_PMessage! =_ nulo)  <br/> |Abra quaisquer objetos incorporados. É garantido que os dados da mensagem armazenada no _PMessage_ sejam iguais à mensagem do [IPersistMessage anterior:: salvar](ipersistmessage-save.md) chamada. Se a chamada **SaveCompleted** for bem-sucedida, insira o estado normal. Caso contrário, defina o último erro como E_OUTOFMEMORY e permaneça no estado HandsOffAfterSave.  <br/> |[Normal](normal-state.md) ou HandsOffAfterSave  <br/> |
|**IPersistMessage:: SaveCompleted** (_PMessage = =_ nulo)  <br/> |Defina o último erro como E_INVALIDARG ou E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md), **salvar**ou [IPersistMessage:: InitNew](ipersistmessage-initnew.md) <br/> |Definir o último erro para e retornar E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Carregar o objeto Form com dados da mensagem de destino. Essa chamada pode ocorrer quando o objeto Form estiver indo para a mensagem seguinte ou anterior em uma pasta.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Retorna o último erro.  <br/> |HandsOffAfterSave  <br/> |
|Outros métodos [IPersistMessage: IUnknown](ipersistmessageiunknown.md) de outras interfaces  <br/> |Definir o último erro para e retornar E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
   
## <a name="see-also"></a>Confira também



[Estados de formulário](form-states.md)

