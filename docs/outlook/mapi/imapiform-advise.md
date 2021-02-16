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
  
Registra um visualizador de formulário para notificações sobre eventos que afetam o formulário.
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a>Parâmetros

 _pAdvise_
  
> [in] Um ponteiro para um objeto sink de exibição aconselha a receber as notificações subsequentes. 
    
 _ligaConnection_
  
> [out] Um ponteiro para um valor que não é zero que representa um registro de notificação bem-sucedido.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro foi bem-sucedido.
    
E_OUTOFMEMORY 
  
> O registro não teve êxito devido a memória insuficiente.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chamam o método **IMAPIForm::Advise** de um formulário para registrar a notificação quando ocorrem alterações no formulário. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Mantenha uma cópia do ponteiro do sink de dica de exibição passado no parâmetro  _pAdvise_ para que você possa usá-lo para chamar o método [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) apropriado quando ocorrer um evento. Chame o método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) do sink de modo de exibição para reter o ponteiro até que o registro de notificação seja cancelado. De definir o conteúdo do  _parâmetroligaConnection_ como um número que não seja zero. 
  
Muitos formulários implementam um objeto auxiliar para manipular o registro e a notificação subsequente de eventos. 
  
Para obter mais informações sobre o processo de notificação em geral, consulte [Notificação de Evento em MAPI](event-notification-in-mapi.md). 
  
Para obter mais informações sobre notificações e formulários, consulte [Enviando e recebendo notificações de formulário.](sending-and-receiving-form-notifications.md)
  
## <a name="see-also"></a>Confira também



[IMAPIForm::Unadvise](imapiform-unadvise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[Notificação de evento em MAPI](event-notification-in-mapi.md)
  
[Enviando e recebendo notificações de formulário](sending-and-receiving-form-notifications.md)

