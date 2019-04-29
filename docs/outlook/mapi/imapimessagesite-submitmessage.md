---
title: IMAPIMessageSiteSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SubmitMessage
api_type:
- COM
ms.assetid: 6b14c383-8bc6-4e86-bd92-0500272af40d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 496732e334d2d39672048dd1a02346aaee4b70e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417025"
---
# <a name="imapimessagesitesubmitmessage"></a>IMAPIMessageSite::SubmitMessage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Solicita que a mensagem atual seja enfileirada para entrega.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Uma bitmask de sinalizadores que controlam como uma mensagem é enviada. O seguinte sinalizador pode ser definido:
    
FORCE_SUBMIT 
  
> O MAPI deve enviar a mensagem mesmo que ela não possa ser enviada imediatamente.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

Os objetos Form chamam o método **IMAPIMessageSite:: SubmitMessage** para solicitar que uma mensagem seja enfileirada para entrega. O site de mensagens deve chamar o método [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) antes de enviar a mensagem. A mensagem não precisa ter sido salva anteriormente porque **SubmitMessage** deve fazer com que a mensagem seja salva se a mensagem tiver sido modificada. Após o retorno de **SubmitMessage**, o formulário deve verificar uma mensagem atual e, em seguida, se descartar, se não houver nenhuma. 
  
Para obter uma lista de interfaces relacionadas a servidores de formulário, consulte [interfaces de formulário MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: SubmitMessage  <br/> |MFCMAPI usa o método **IMAPIMessageSite:: SubmitMessage** para salvar a mensagem. Primeiro, ele chama o método **IPersistMessage:: HandsOffMessage** e, em seguida, chama **SubmitMessage**.  <br/> |
   
## <a name="see-also"></a>Confira também



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulário MAPI](mapi-form-interfaces.md)

