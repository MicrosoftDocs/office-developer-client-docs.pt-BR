---
title: Estado Uninitialized
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 95ed80a6d0ea6a6a7c8cc768b32981ac899b69e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578245"
---
# <a name="uninitialized-state"></a>Estado Uninitialized

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O estado não inicializado é o formulário de estado inicial objetos devem estar no quando forem criados pela primeira vez. Objetos de formulário se tornam inicializados com dados de mensagem quando um aplicativo cliente chama o método [IPersistMessage::InitNew](ipersistmessage-initnew.md) ou [IPersistMessage::Load](ipersistmessage-load.md) no objeto de formulário. A tabela a seguir descreve as transições permitidas do estado de Unitialized. 
  
|**Método IPersistMessage**|**Action**|**Novo estado**|
|:-----|:-----|:-----|
|[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Carregar o objeto de formulário com os dados padrão.  <br/> |[Normal](normal-state.md) <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Carregar o objeto de formulário com os dados da mensagem de destino.  <br/> |Normal  <br/> |
|[IPersistMessage::GetClassID](ipersistmessage-getclassid.md) <br/> |Retornar o sucesso, ou definir o último erro como e retornar E_UNEXPECTED.  <br/> |Não inicializado  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Retorna o último erro.  <br/> |Não inicializado  <br/> |
|Outros [IPersistMessage: IUnknown](ipersistmessageiunknown.md) métodos ou métodos de outras interfaces  <br/> |Defina o último erro como e retornar E_UNEXPECTED.  <br/> |Não inicializado  <br/> |
   
## <a name="see-also"></a>Confira também



[Estado Normal](normal-state.md)
  
[Estados de formulários](form-states.md)

