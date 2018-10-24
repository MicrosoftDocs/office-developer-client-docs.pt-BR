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
ms.openlocfilehash: 202d461d4acefe18e69b47db9319cb328c61406e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592315"
---
# <a name="imapiviewadvisesinkonprint"></a>IMAPIViewAdviseSink::OnPrint

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Notifica o Visualizador de formulário do status impressão de um formulário.
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a>Parâmetros

 _dwPageNumber_
  
> [in] Número da última página impressa.
    
 _hsStatus diferente_
  
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
  
> O usuário cancelou a operação, geralmente clicando no botão Cancelar em uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

Objetos de formulário chame o método de **IMAPIViewAdviseSink::OnPrint** durante a impressão para informar o Visualizador do progresso da impressão. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se o trabalho de impressão envolve várias páginas, é possível chamar **OnPrint** após cada página ser impressa. Definir _dwPageNumber_ para a página que está sendo impressa no momento e _hsStatus diferente_ para S_OK. Quando o trabalho de impressão estiver concluído, chamada **OnPrint** com _dwPageNumber_ definido para a última página impressa e _hsStatus diferente_ definido como S_FALSE. 
  
Para obter mais informações sobre as notificações do formulário, consulte [de envio e recebimento de notificações de formulário](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Confira também



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

