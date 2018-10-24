---
title: IMAPIFormUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Unadvise
api_type:
- COM
ms.assetid: fdda45e2-631d-404c-8af4-bce68df0968b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 770ceb7af98f5271baad65043e013feb353d231a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390468"
---
# <a name="imapiformunadvise"></a>IMAPIForm::Unadvise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cancela um registro para notificações com um visualizador de formulário que tenha estabelecido chamando [IMAPIForm::Advise](imapiform-advise.md).
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Par�metros

 _ulConnection_
  
> [in] Um número de conexão que identifica o registro de notificação para ser cancelado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro foi cancelado.
    
E_INVALIDARG 
  
> O número de conexão passado no parâmetro _ulConnection_ não representa um registro válido. 
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chame o método de **IMAPIForm::Unadvise** para cancelar um registro de notificação de que eles estabelecerem primeiramente chamando o método **IMAPIForm::Advise** . 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Descartar o ponteiro que você está mantendo ao modo de exibição do visualizador formulário aconselhe coletor de eventos chamando o método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) . Geralmente, a **versão** é chamado durante a chamada **Unadvise** . No entanto, se outro thread está em processo de chamar um dos métodos [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) coletor de eventos de aviso para o modo de exibição, atrasar a chamada de **liberação** até que o método **IMAPIViewAdviseSink** retorna. 
  
## <a name="see-also"></a>Confira também



[IMAPIForm::Advise](imapiform-advise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

