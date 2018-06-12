---
title: IMAPIViewAdviseSinkOnSaved
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSaved
api_type:
- COM
ms.assetid: c327e31a-7b62-4e21-9b69-b27442f1eaca
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 0f9aa5d508afeaf5933c50763e1e42832ae4e3f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767364"
---
# <a name="imapiviewadvisesinkonsaved"></a>IMAPIViewAdviseSink::OnSaved

  
  
**Aplica-se a**: Outlook 
  
Notifica o Visualizador de formulário que tenha sido salva a mensagem atual em um formulário.
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a>Parâmetros

None
  
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Coment�rios

Um objeto form chama o método **IMAPIViewAdviseSink::OnSaved** depois que a mensagem atual em um formulário foi salvo com êxito. Isso permite que os visualizadores atualizam suas janelas para refletir as alterações à mensagem. 
  
Para obter mais informações sobre as notificações do formulário, consulte [de envio e recebimento de notificações de formulário](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Confira também



[IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)

