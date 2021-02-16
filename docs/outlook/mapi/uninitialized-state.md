---
title: Estado Não Reinicializado
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
# <a name="uninitialized-state"></a>Estado Não Reinicializado

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O estado Não inicializado é o estado inicial em que os objetos de formulário de estado devem estar quando são criados pela primeira vez. Objetos de formulário são inicializados com dados de mensagem quando um aplicativo cliente chama o método [IPersistMessage::InitNew](ipersistmessage-initnew.md) ou [IPersistMessage::Load](ipersistmessage-load.md) no objeto de formulário. A tabela a seguir descreve transições permitidas do estado Unitializado. 
  
|**Método IPersistMessage**|**Ação**|**Novo estado**|
|:-----|:-----|:-----|
|[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Carregar o objeto de formulário com dados padrão.  <br/> |[Normal](normal-state.md) <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Carregue o objeto de formulário com dados da mensagem de destino.  <br/> |Normal  <br/> |
|[IPersistMessage::GetClassID](ipersistmessage-getclassid.md) <br/> |Retornar sucesso ou definir o último erro para e retornar E_UNEXPECTED.  <br/> |Não reinicializado  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Retornar o último erro.  <br/> |Não reinicializado  <br/> |
|Outros [IPersistMessage : métodos ou métodos IUnknown](ipersistmessageiunknown.md) de outras interfaces  <br/> |De definida a última mensagem de erro e retorne E_UNEXPECTED.  <br/> |Não reinicializado  <br/> |
   
## <a name="see-also"></a>Confira também



[Estado Normal](normal-state.md)
  
[Estados do formulário](form-states.md)

