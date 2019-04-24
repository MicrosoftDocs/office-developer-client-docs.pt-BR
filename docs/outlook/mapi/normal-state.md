---
title: Estado normal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b2acad7-5ef8-44db-911f-3bd2a7ca2778
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d7b50a92c58dd7ab1f03cb4cf84acc2d4a2b404b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335739"
---
# <a name="normal-state"></a>Estado normal

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O estado normal é onde o objeto Form gasta a maior parte do tempo, esperando que os aplicativos clientes iniciem uma ação, como salvar alterações ou fechar o formulário. A tabela a seguir descreve as transições permitidas do estado normal.
  
|**Método IPersistMessage**|**Action**|**Novo estado**|
|:-----|:-----|:-----|
|[IPersistMessage:: salvar](ipersistmessage-save.md) (_PMessage = =_ nulo, _fSameAsLoad = =_ true)  <br/> - ou -  <br/> **IPersistMessage:: salvar** (_PMessage! =_ nulo, _fSameAsLoad = =_ false)  <br/> |Salvar recursivamente todos os objetos OLE incorporados que foram modificados. Salve os dados da mensagem de volta para o objeto Message. Armazene o sinalizador _fSameAsLoad_ para uso posterior no [](noscribble-state.md) estado norabisco.  <br/> |NoScribble  <br/> |
|**IPersistMessage:: salvar** (_PMessage! =_ nulo, _fSameAsLoad = =_ true)  <br/> |É o mesmo que o caso anterior, exceto pelo fato de que essa chamada **salva** é usada em situações de pouca memória e não deve falhar por falta de memória.  <br/> |NoScribble  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Invocar recursivamente o método **HandsOffMessage** em mensagens incorporadas ou o método OLE [IPersistStorage:: HANDSOFFSTORAGE](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) em objetos OLE incorporados. Liberar o objeto Message e quaisquer mensagens ou objetos incorporados.  <br/> |[HandsOffFromNormal](handsofffromnormal-state.md) <br/> |
|[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage:: InitNew](ipersistmessage-initnew.md) ou [IPersistMessage:: Load](ipersistmessage-load.md) <br/> |Definir o último erro para e retornar E_UNEXPECTED.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Retorna o último erro.  <br/> |Normal  <br/> |
|Outros métodos [IPersistMessage: IUnknown](ipersistmessageiunknown.md) de outras interfaces  <br/> |Implemente conforme descrito na documentação da interface [IPersistMessage: IUnknown](ipersistmessageiunknown.md) .  <br/> |Normal  <br/> |
   
## <a name="see-also"></a>Confira também



[Estados de formulário](form-states.md)

