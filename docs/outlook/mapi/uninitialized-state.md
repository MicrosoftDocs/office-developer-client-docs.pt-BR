---
title: Estado não inicializado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: be35c9d3f8fc7badf83086e63e4c94e0efa4d5bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425558"
---
# <a name="uninitialized-state"></a>Estado não inicializado

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O estado não inicializado é o objeto de formulário de estado inicial que deve ser quando criados pela primeira vez. Os objetos Form são inicializados com dados de mensagem quando um aplicativo cliente chama o método [IPersistMessage:: InitNew](ipersistmessage-initnew.md) ou [IPersistMessage:: Load](ipersistmessage-load.md) no objeto Form. A tabela a seguir descreve as transições permitidas do estado unitialized. 
  
|**Método IPersistMessage**|**Action**|**Novo estado**|
|:-----|:-----|:-----|
|[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Carregar o objeto Form com dados padrão.  <br/> |[Normal](normal-state.md) <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Carregar o objeto Form com dados da mensagem de destino.  <br/> |Normal  <br/> |
|[IPersistMessage::GetClassID](ipersistmessage-getclassid.md) <br/> |Retornar êxito ou definir o último erro para e retornar E_UNEXPECTED.  <br/> |Não inicializado  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Retorna o último erro.  <br/> |Não inicializado  <br/> |
|Outros métodos [IPersistMessage: IUnknown](ipersistmessageiunknown.md) de outras interfaces  <br/> |Definir o último erro para e retornar E_UNEXPECTED.  <br/> |Não inicializado  <br/> |
   
## <a name="see-also"></a>Confira também



[Estado normal](normal-state.md)
  
[Estados de formulário](form-states.md)

