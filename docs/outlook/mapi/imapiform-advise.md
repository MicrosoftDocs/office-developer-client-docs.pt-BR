---
title: IMAPIFormAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Advise
api_type:
- COM
ms.assetid: 961318d6-bebe-4f4b-98ff-921cafc68d24
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b5347205e10b44d62a7e11cbe2f4179970f1bd64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766990"
---
# <a name="imapiformadvise"></a>IMAPIForm::Advise

  
  
**Aplica-se a**: Outlook 
  
Registra um visualizador de formulário para notificações de eventos que afetam o formulário.
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a>Par�metros

 _pAdvise_
  
> [in] Um ponteiro para um modo de exibição avise o objeto coletor de eventos para receber as notificações subsequentes. 
    
 _pulConnection_
  
> [out] Um ponteiro para um valor diferente de zero que representa um registro de notificação bem-sucedida.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O registro foi bem-sucedida.
    
E_OUTOFMEMORY 
  
> O registro não foi bem-sucedida devido a memória insuficiente.
    
## <a name="remarks"></a>Coment�rios

Visualizadores de formulário chame o método de **IMAPIForm::Advise** de um formulário para registrar a notificação quando ocorrem alterações ao formulário. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

O ponteiro do coletor de eventos passada no parâmetro _pAdvise_ para que você pode usá-lo para chamar o método [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) apropriado quando ocorre um evento de aviso de manter uma cópia do modo de exibição. O modo de exibição de chamada de aviso de método do coletor de [AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) para reter o ponteiro até que o registro de notificação será cancelado. Defina o conteúdo do parâmetro _pulConnection_ para um número diferente de zero. 
  
Formulários muitas implementam um objeto auxiliar para manipular o registro e as notificações subsequentes de eventos. 
  
Para obter mais informações sobre o processo de notificação em geral, consulte a [Notificação de evento em MAPI](event-notification-in-mapi.md). 
  
Para obter mais informações sobre a notificação e formulários, consulte [de envio e recebimento de notificações de formulário](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Confira também



[IMAPIForm::Unadvise](imapiform-unadvise.md)
  
[IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm: IUnknown](imapiformiunknown.md)


[Notificação de evento em MAPI](event-notification-in-mapi.md)
  
[Enviando e recebendo notificações de formulário](sending-and-receiving-form-notifications.md)

