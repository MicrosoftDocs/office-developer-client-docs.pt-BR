---
title: Estado NoScribble
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0246138f-c55e-4353-8e53-e973f524d52c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 41f5acddf273de39a7d5952ccb00e868170c692d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768161"
---
# <a name="noscribble-state"></a>Estado NoScribble

  
  
**Aplica-se a**: Outlook 
  
O estado de NoScribble indica que as alterações a uma mensagem estão sendo salva. O salvamento real dos valores armazenados na interface do usuário do objeto form ocorre quando o formulário método do objeto [IPersistMessage::Save](ipersistmessage-save.md) é chamado pelo aplicativo cliente. A tabela a seguir descreve as transições permitidas do estado de NoScribble. 
  
|IPersistMessage * * método * *|**Action**|**Novo estado**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage = =_ nulo)  <br/> |Se o sinalizador _fSameAsLoad_ foi TRUE na chamada [IPersistMessage::Save](ipersistmessage-save.md) que causou o formulário para inserir o estado de NoScribble e a mensagem foi modificada, internamente marcar como salva as alterações e chamar o [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) método.  <br/> |[Normal](normal-state.md) <br/> |
|**IPersistMessage::SaveCompleted** (_pMessage! =_ nulo)  <br/> |Chame o método de [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) (semelhante ao método OLE [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) ) seguido as ações de **SaveCompleted** normais. Se **SaveCompleted** foi bem-sucedida, insira o estado Normal. Caso contrário, insira o estado de [HandsOffAfterSave](handsoffaftersave-state.md) .  <br/> |Normal ou HandsOffAfterSave  <br/> |
|**HandsOffMessage** <br/> |Recursivamente chamar o método **HandsOffMessage** em mensagens inseridas ou o método de OLE **IPersistStorage::HandsOffStorage** nos objetos OLE incorporados. Libere o objeto de mensagem e qualquer mensagens inseridas ou objeto.  <br/> |HandsOffAfterSave  <br/> |
|**Salvar**, [IPersistMessage::InitNew](ipersistmessage-initnew.md)ou [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Defina o último erro como e retornar E_UNEXPECTED.  <br/> |NoScribble  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Retorna o último erro.  <br/> |NoScribble  <br/> |
|Outros [IPersistMessage: IUnknown](ipersistmessageiunknown.md) métodos ou métodos de outras interfaces  <br/> |Defina o último erro como e retornar E_UNEXPECTED.  <br/> |NoScribble  <br/> |
   
## <a name="see-also"></a>Confira também



[Estados de formulários](form-states.md)

