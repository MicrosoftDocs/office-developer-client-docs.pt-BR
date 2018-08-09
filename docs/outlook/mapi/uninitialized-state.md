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
ms.openlocfilehash: c00d5bb2e5da02b007579c7a8206baa98f64143f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770656"
---
# <a name="uninitialized-state"></a>Estado Uninitialized

  
  
**Aplica-se a**: Outlook 
  
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

