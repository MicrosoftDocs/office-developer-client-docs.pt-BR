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
ms.openlocfilehash: d7b50a92c58dd7ab1f03cb4cf84acc2d4a2b404b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335739"
---
# <a name="normal-state"></a>Estado Normal

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O estado Normal é onde o objeto de formulário passa a maior parte do tempo, aguardando que os aplicativos cliente iniciem uma ação como salvar alterações ou fechar o formulário. A tabela a seguir descreve transições permitidas do estado Normal.
  
|**Método IPersistMessage**|**Ação**|**Novo estado**|
|:-----|:-----|:-----|
|[IPersistMessage::Save](ipersistmessage-save.md)(_pMessage ==_ NULL,  _fSameAsLoad ==_ TRUE)  <br/> - ou -  <br/> **IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ FALSE)  <br/> |Salve recursivamente quaisquer objetos OLE incorporados que tenham sido modificados. Salve os dados da mensagem de volta no objeto de mensagem. Armazene _o sinalizador fSameAsLoad_ para uso posterior no [estado NoScribble.](noscribble-state.md)  <br/> |NoScribble  <br/> |
|**IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ TRUE)  <br/> |Esse é o mesmo caso anterior, exceto pelo fato de que essa chamada **Salvar** é usada em situações de pouca memória e não deve falhar por falta de memória.  <br/> |NoScribble  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Invoque recursivamente o método **HandsOffMessage** em mensagens incorporadas ou o método [OLE IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) em objetos OLE incorporados. Liberar o objeto de mensagem e quaisquer mensagens ou objetos incorporados.  <br/> |[HandsOffFromNormal](handsofffromnormal-state.md) <br/> |
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md) ou [IPersistMessage::Load](ipersistmessage-load.md) <br/> |De definida a última mensagem de erro e retorne E_UNEXPECTED.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Retornar o último erro.  <br/> |Normal  <br/> |
|Outros [IPersistMessage : métodos ou métodos IUnknown](ipersistmessageiunknown.md) de outras interfaces  <br/> |Implemente conforme descrito na documentação para [a interface IPersistMessage : IUnknown.](ipersistmessageiunknown.md)  <br/> |Normal  <br/> |
   
## <a name="see-also"></a>Confira também



[Estados do formulário](form-states.md)

