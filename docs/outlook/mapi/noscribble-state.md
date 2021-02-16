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
ms.openlocfilehash: 239f11cf27cdebff3d51645319d7ada3b9bb9ff6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326198"
---
# <a name="noscribble-state"></a>Estado NoScribble

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O estado NoScribble indica que as alterações em uma mensagem estão sendo salvas. O real salvar dos valores armazenados na interface do usuário do objeto de formulário ocorre quando o método [IPersistMessage::Save](ipersistmessage-save.md) do objeto de formulário é chamado pelo aplicativo cliente. A tabela a seguir descreve transições permitidas do estado NoScribble. 
  
|Método IPersistMessage**|**Ação**|**Novo estado**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage ==_ NULL)  <br/> |Se o sinalizador _fSameAsLoad_ foi VERDADEIRO na chamada [IPersistMessage::Save](ipersistmessage-save.md) que fez com que o formulário inscrevesse o estado NoScribble e a mensagem tivesse sido modificada, marque internamente as alterações como salvas e chame o método [IMAPIViewAdviseSink::OnSaved.](imapiviewadvisesink-onsaved.md)  <br/> |[Normal](normal-state.md) <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage !=_ NULL)  <br/> |Chame o método [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) (semelhante ao método [OLE IPersistStorage::HandsOffStorage)](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) seguido pelas ações **SaveCompleted** normais. Se **SaveCompleted** foi bem-sucedido, insira o estado Normal. Caso contrário, insira [o estado HandsOffAfterSave.](handsoffaftersave-state.md)  <br/> |Normal ou HandsOffAfterSave  <br/> |
|**HandsOffMessage** <br/> |Invoque recursivamente o método **HandsOffMessage** em mensagens incorporadas ou o método **OLE IPersistStorage::HandsOffStorage** em objetos OLE incorporados. Libere o objeto message e quaisquer mensagens ou objetos incorporados.  <br/> |HandsOffAfterSave  <br/> |
|**Save**, [IPersistMessage::InitNew](ipersistmessage-initnew.md)ou [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Definir o último erro e retornar E_UNEXPECTED.  <br/> |NoScribble  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Retornar o último erro.  <br/> |NoScribble  <br/> |
|Outros [IPersistMessage : métodos ou métodos IUnknown](ipersistmessageiunknown.md) de outras interfaces  <br/> |Definir o último erro e retornar E_UNEXPECTED.  <br/> |NoScribble  <br/> |
   
## <a name="see-also"></a>Confira também



[Estados do formulário](form-states.md)

