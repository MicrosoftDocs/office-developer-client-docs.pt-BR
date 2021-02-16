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
ms.openlocfilehash: f6cdebf82d8b84ada3d029865867c5192af90b0d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409906"
---
# <a name="imapisupportspooleryield"></a>IMAPISupport::SpoolerYield

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Dá controle da CPU ao spooler MAPI para que ele possa executar todas as tarefas que considera necessárias.
  
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
  
> O provedor de transporte lançou com êxito a CPU.
    
MAPI_W_CANCEL_MESSAGE 
  
> Instrui o provedor de transporte a interromper a entrega da mensagem para todos os destinatários que ainda não a receberam.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::SpoolerYield** é implementado para objetos de suporte do provedor de transporte. Os provedores de transporte **chamam SpoolerYield** para permitir que o spooler MAPI realize qualquer processamento necessário. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame **SpoolerYield** quando estiver executando operações demoradas que podem ser pausadas. Isso permite que aplicativos em primeiro plano executem durante uma longa operação, como a entrega para uma lista de destinatários grande em uma rede ocupada. 
  
Se **SpoolerYield** retornar com MAPI_W_CANCEL_MESSAGE, o spooler MAPI determinou que a mensagem não deve mais ser enviada. Retorne MAPI_E_USER_CANCEL processo de chamada e saia, se possível. 
  
Para obter mais informações sobre como gerar para o spooler MAPI, consulte [Interagindo com o Spooler MAPI.](interacting-with-the-mapi-spooler.md)
  
## <a name="see-also"></a>Confira também



[IMAPISupport: IUnknown](imapisupportiunknown.md)

