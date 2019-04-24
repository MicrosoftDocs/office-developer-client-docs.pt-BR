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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2ed8bace97dee3842243ed835769e80e8aaf6b03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329481"
---
# <a name="imapiformadvise"></a>IMAPIForm::Advise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra um visualizador de formulários para notificações sobre eventos que afetam o formulário.
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a>Parâmetros

 _pAdvise_
  
> no Um ponteiro para um objeto de coletor de aviso de exibição para receber as notificações subsequentes. 
    
 _pulConnection_
  
> bota Um ponteiro para um valor diferente de zero que representa um registro de notificação bem-sucedido.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro foi bem-sucedido.
    
E_OUTOFMEMORY 
  
> O registro não foi bem-sucedido devido à memória insuficiente.
    
## <a name="remarks"></a>Comentários

Os visualizadores de formulários chamam o método **IMAPIForm:: Advise** de um formulário para registrar a notificação quando ocorrerem alterações no formulário. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Mantenha uma cópia do ponteiro View Advise Sink passado no parâmetro _pAdvise_ para que você possa usá-lo para chamar o método [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) apropriado quando ocorre um evento. Chame o método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) do coletor de avisos de exibição para manter o ponteiro até que o registro de notificação seja cancelado. Defina o conteúdo do parâmetro _pulConnection_ para um número diferente de zero. 
  
Muitos formulários implementam um objeto auxiliar para lidar com o registro e a notificação subsequente de eventos. 
  
Para obter mais informações sobre o processo de notificação em geral, consulte [Event Notification in MAPI](event-notification-in-mapi.md). 
  
Para obter mais informações sobre notificações e formulários, consulte [envio e recebimento de notificações de formulários](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Confira também



[IMAPIForm::Unadvise](imapiform-unadvise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[Notificação de evento no MAPI](event-notification-in-mapi.md)
  
[Enviar e receber notificações de formulário](sending-and-receiving-form-notifications.md)

