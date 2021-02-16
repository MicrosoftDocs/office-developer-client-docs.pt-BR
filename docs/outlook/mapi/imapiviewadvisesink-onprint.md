---
title: IMAPIViewAdviseSinkOnPrint
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnPrint
api_type:
- COM
ms.assetid: d16219a0-268c-428d-9f02-4f06eb5b6d7d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e66315042f8b5cd5aff0e4aa076588c9f312376a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406168"
---
# <a name="imapiviewadvisesinkonprint"></a>IMAPIViewAdviseSink::OnPrint

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Notifica o visualizador de formulário sobre o status de impressão de um formulário.
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a>Parâmetros

 _dwPageNumber_
  
> [in] Número da última página impressa.
    
 _hrStatus_
  
> [in] Um valor HRESULT que indica o status do trabalho de impressão. Os valores possíveis são:
    
S_FALSE 
  
> O trabalho de impressão foi concluído com êxito.
    
S_OK 
  
> O trabalho de impressão está em andamento.
    
FALHA 
  
> O trabalho de impressão foi encerrado devido a uma falha.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A notificação foi bem-sucedida.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, normalmente clicando no botão Cancelar em uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

Os objetos de formulário chamam o método **IMAPIViewAdviseSink::OnPrint** durante a impressão para informar o visualizador sobre o progresso da impressão. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se o trabalho de impressão envolver várias páginas, você poderá chamar **OnPrint** depois que cada página for impressa. De  _definir dwPageNumber_ como a página que está sendo impressa no momento e  _hrStatus_ como S_OK. Quando o trabalho de impressão for concluído, chame **OnPrint** com  _dwPageNumber_ definida como a última página impressa e  _hrStatus_ definida como S_FALSE. 
  
Para obter mais informações sobre notificações de formulário, consulte [Envio e recebimento de notificações de formulário.](sending-and-receiving-form-notifications.md)
  
## <a name="see-also"></a>Confira também



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

