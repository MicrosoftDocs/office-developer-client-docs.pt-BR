---
title: IMAPISupportSpoolerYield
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerYield
api_type:
- COM
ms.assetid: f5c6ba8f-4ef5-4d60-b4e6-5b9160ec4e99
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d90f502e2cd7f97ac273ebecedbd0363097b1d60
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584951"
---
# <a name="imapisupportspooleryield"></a>IMAPISupport::SpoolerYield

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece o controle da CPU para o spooler MAPI para que ele pode executar qualquer tarefa que ele considera necessário.
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> Reservado; deve ser zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O provedor de transporte com êxito liberado da CPU.
    
MAPI_W_CANCEL_MESSAGE 
  
> Instrui o provedor de transporte para interromper a entrega da mensagem para qualquer destinatários que ainda não recebeu-lo.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::SpoolerYield** é implementado para objetos de suporte do provedor de transporte. Provedores de transporte chamarem **SpoolerYield** para permitir que o spooler MAPI realizar qualquer processamento necessário. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame **SpoolerYield** quando você estiver executando operações demoradas que podem ser pausadas. Isso permite que aplicativos de primeiro plano para serem executados durante uma operação longa, como entrega para uma grande lista de destinatários em uma rede ocupada. 
  
Se **SpoolerYield** retornar com MAPI_W_CANCEL_MESSAGE, o MAPI spooler determinou que a mensagem não é mais deve ser enviada. Retorne MAPI_E_USER_CANCEL ao seu processo de chamada e a saída, se possível. 
  
Para obter mais informações sobre como resultando no MAPI spooler, consulte [interagindo com o Spooler de MAPI](interacting-with-the-mapi-spooler.md).
  
## <a name="see-also"></a>Confira também



[IMAPISupport: IUnknown](imapisupportiunknown.md)

