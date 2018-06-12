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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 694ee8b12b9918502e60c0c6ea92992cc1062945
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767098"
---
# <a name="imapimessagesitesubmitmessage"></a>IMAPIMessageSite::SubmitMessage

  
  
**Aplica-se a**: Outlook 
  
Solicita que a mensagem atual ser colocados na fila de entrega.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como uma mensagem é enviada. O seguinte sinalizador pode ser definido:
    
FORCE_SUBMIT 
  
> MAPI deve enviar a mensagem, mesmo que não podem ser enviado imediatamente.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Coment�rios

Objetos de formulário chame o método de **IMAPIMessageSite::SubmitMessage** para solicitar que uma mensagem ser colocados na fila de entrega. O site de mensagem deve chamar o método [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) antes de enviar a mensagem. A mensagem não precisa tenha sido salva anteriormente, porque **SubmitMessage** deve fazer com que a mensagem a ser salvo se a mensagem tiver sido modificada. Após o retorno de **SubmitMessage**, o formulário deve verificar se há uma mensagem atual e, em seguida, descartar a próprio se não houver nenhum. 
  
Para obter uma lista das interfaces relacionadas aos servidores de formulário, consulte [Interfaces de formulário de MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SubmitMessage  <br/> |MFCMAPI usa o método **IMAPIMessageSite::SubmitMessage** para salvar a mensagem. Primeiro, ele chama o método **IPersistMessage::HandsOffMessage** e, em seguida, ele chama **SubmitMessage**.  <br/> |
   
## <a name="see-also"></a>Confira também



[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulário MAPI](mapi-form-interfaces.md)

