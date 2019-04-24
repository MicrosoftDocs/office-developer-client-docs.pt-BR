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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329467"
---
# <a name="imapiformunadvise"></a>IMAPIForm::Unadvise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cancela um registro de notificações com um visualizador de formulários estabelecido anteriormente chamando [IMAPIForm:: Advise](imapiform-advise.md).
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parâmetros

 _ulConnection_
  
> no Um número de conexão que identifica o registro de notificação a ser cancelado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro foi cancelado.
    
E_INVALIDARG 
  
> O número de conexão passado no parâmetro _ulConnection_ não representa um registro válido. 
    
## <a name="remarks"></a>Comentários

Os visualizadores de formulários chamam o método **IMAPIForm:: Unadvise** para cancelar um registro para notificação de que ele primeiro estabeleceu chamando o método **IMAPIForm:: Advise** . 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

DesCartar o ponteiro que você está segurando para o coletor de aviso de exibição do Visualizador de formulários chamando seu método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) . Geralmente, o **lançamento** é chamado durante a chamada de **Unadvise** . No enTanto, se outro thread estiver no processo de chamar um dos métodos [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) para o coletor de aviso de exibição, adie a chamada de **lançamento** até que o método **IMAPIViewAdviseSink** retorne. 
  
## <a name="see-also"></a>Confira também



[IMAPIForm::Advise](imapiform-advise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

