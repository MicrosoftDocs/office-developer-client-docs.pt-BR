---
title: Estado Normal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b2acad7-5ef8-44db-911f-3bd2a7ca2778
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d5c92c243069e5b8b500df086169c8e5b961976d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570713"
---
# <a name="normal-state"></a>Estado Normal

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O estado Normal é onde o objeto form passa a maior parte de seu tempo, aguardando para aplicativos de cliente para iniciar uma ação como salvar as alterações ou fechar o formulário. A tabela a seguir descreve as transições permitidas do estado Normal.
  
|**Método IPersistMessage**|**Action**|**Novo estado**|
|:-----|:-----|:-----|
|[IPersistMessage::Save](ipersistmessage-save.md) (_pMessage = =_ nula _fSameAsLoad = =_ TRUE)  <br/> -ou-  <br/> **IPersistMessage::Save** (_pMessage! =_ nula _fSameAsLoad = =_ falso)  <br/> |Recursivamente salvar quaisquer objetos OLE incorporados que foram modificados. Salve dados de mensagem volta para o objeto de mensagem. Armazene o sinalizador _fSameAsLoad_ para uso posterior no estado [NoScribble](noscribble-state.md) .  <br/> |NoScribble  <br/> |
|**IPersistMessage::Save** (_pMessage! =_ nula _fSameAsLoad = =_ TRUE)  <br/> |Isso é o mesmo caso anterior, exceto pelo fato dessa chamada **Salvar** é usada em situações de pouca memória e não deve transferir por falta de memória.  <br/> |NoScribble  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Recursivamente chamar o método **HandsOffMessage** em mensagens inseridas ou o método de OLE [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) nos objetos OLE incorporados. Libere o objeto de mensagem e qualquer mensagens inseridas ou objeto.  <br/> |[HandsOffFromNormal](handsofffromnormal-state.md) <br/> |
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md) ou [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Defina o último erro como e retornar E_UNEXPECTED.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Retorna o último erro.  <br/> |Normal  <br/> |
|Outros [IPersistMessage: IUnknown](ipersistmessageiunknown.md) métodos ou métodos de outras interfaces  <br/> |Implementar conforme descrito na documentação para o [IPersistMessage: IUnknown](ipersistmessageiunknown.md) interface.  <br/> |Normal  <br/> |
   
## <a name="see-also"></a>Confira também



[Estados de formulários](form-states.md)

