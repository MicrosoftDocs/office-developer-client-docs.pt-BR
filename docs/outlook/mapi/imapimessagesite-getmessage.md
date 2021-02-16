---
title: IMAPIMessageSiteGetMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetMessage
api_type:
- COM
ms.assetid: 49d12c49-84f8-44ac-bc4a-2ee44a46f8c1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 03dd0553d0203585850ac5c4f8c91c86ef60236a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409024"
---
# <a name="imapimessagesitegetmessage"></a>IMAPIMessageSite::GetMessage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna a mensagem atual.
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>Parâmetros

 _ppmsg_
  
> [out] Um ponteiro para um ponteiro para a interface retornada da mensagem.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
S_FALSE 
  
> No momento, não existe nenhuma mensagem para o formulário de chamada.
    
## <a name="remarks"></a>Comentários

Os formulários chamam **o método IMAPIMessageSite::GetMessage** para obter uma interface de mensagem para a mensagem atual. A mensagem atual é a mesma que foi passada anteriormente no [método IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md)ou [IPersistMessage::SaveCompleted.](ipersistmessage-savecompleted.md) 
  
 **GetMessage** retornará S_FALSE se nenhuma mensagem existir no momento. Esse estado pode ocorrer após chamadas para o método [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) ou antes da próxima chamada para **IPersistMessage::Load** ou **IPersistMessage::SaveCompleted** ser feita. 
  
Para uma lista de interfaces relacionadas a servidores de formulário, consulte [MAPI Form Interfaces](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSession  <br/> |MFCMAPI usa o método **IMAPIMessageSite::GetMessage** para retornar o ponteiro da mensagem atualmente armazenado em cache, se ele estiver disponível.  <br/> |
   
## <a name="see-also"></a>Confira também



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulário MAPI](mapi-form-interfaces.md)

