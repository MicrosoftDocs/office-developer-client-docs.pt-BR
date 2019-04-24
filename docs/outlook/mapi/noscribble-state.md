---
title: Estado noRabisco
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0246138f-c55e-4353-8e53-e973f524d52c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 239f11cf27cdebff3d51645319d7ada3b9bb9ff6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326198"
---
# <a name="noscribble-state"></a>Estado noRabisco

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O estado noRabisco indica que as alterações em uma mensagem estão sendo salvas. O salvamento real dos valores armazenados na interface de usuário do objeto Form ocorre quando o método [IPersistMessage:: Save](ipersistmessage-save.md) do objeto Form é chamado pelo aplicativo cliente. A tabela a seguir descreve as transições permitidas do estado noRabisco. 
  
|IPersistMessage * * método * *|**Action**|**Novo estado**|
|:-----|:-----|:-----|
|[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) (_PMessage = =_ nulo)  <br/> |Se o sinalizador _fSameAsLoad_ for true no [IPersistMessage:: Save](ipersistmessage-save.md) Call que fez com que o formulário entraSse no estado norabisco e a mensagem tiver sido modificada, marque internamente as alterações como salvas e chame o [IMAPIViewAdviseSink::](imapiviewadvisesink-onsaved.md) onsaved IME.  <br/> |[Normal](normal-state.md) <br/> |
|**IPersistMessage:: SaveCompleted** (_PMessage! =_ nulo)  <br/> |Chame o método [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) (semelhante ao método OLE [IPersistStorage:: HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) ) seguido pelas ações do **SaveCompleted** normal. Se o **SaveCompleted** tiver sido bem-sucedido, insira o estado normal. Caso contrário, insira o estado [HandsOffAfterSave](handsoffaftersave-state.md) .  <br/> |Normal ou HandsOffAfterSave  <br/> |
|**HandsOffMessage** <br/> |Invocar recursivamente o método **HandsOffMessage** em mensagens incorporadas ou o método OLE **IPersistStorage:: HANDSOFFSTORAGE** em objetos OLE incorporados. Liberar o objeto Message e quaisquer mensagens ou objetos incorporados.  <br/> |HandsOffAfterSave  <br/> |
|**Salvar**, [IPersistMessage:: InitNew](ipersistmessage-initnew.md)ou [IPersistMessage:: Load](ipersistmessage-load.md) <br/> |Definir o último erro para e retornar E_UNEXPECTED.  <br/> |NoScribble  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Retorna o último erro.  <br/> |NoScribble  <br/> |
|Outros métodos [IPersistMessage: IUnknown](ipersistmessageiunknown.md) de outras interfaces  <br/> |Definir o último erro para e retornar E_UNEXPECTED.  <br/> |NoScribble  <br/> |
   
## <a name="see-also"></a>Confira também



[Estados de formulário](form-states.md)

