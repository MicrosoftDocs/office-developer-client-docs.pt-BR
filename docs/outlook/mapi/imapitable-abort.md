---
title: IMAPITableAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Abort
api_type:
- COM
ms.assetid: 73291a5b-b626-494c-b5d9-f7709e34bac2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 68d40a6e152698554fcb88c6f7e5bfd4a7ff0ce3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574003"
---
# <a name="imapitableabort"></a>IMAPITable::Abort

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Interrompe a qualquer operação assíncrona em andamento atualmente para a tabela.
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a>Parâmetros

Nenhum
  
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Uma ou mais operações assíncronas foram interrompidas.
    
MAPI_E_UNABLE_TO_ABORT 
  
> Uma operação assíncrona está em andamento e não pode ser parada ou já foi concluída.
    
## <a name="remarks"></a>Comentários

O método **IMAPITable::Abort** interrompe qualquer operação assíncrona que está em andamento. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para descobrir se uma operação assíncrona está em andamento, chame o método [IMAPITable::GetStatus](imapitable-getstatus.md) . 
  
Se **Anular** interrompe o processamento de uma chamada para o método [IMAPITable:: Restrict](imapitable-restrict.md) , o estado da tabela será como era no momento em que a chamada **Anular** é processada. 
  
Se **Anular** interrompe o processamento de uma chamada para o método [IMAPITable:: SortTable](imapitable-sorttable.md) , ordem de classificação da tabela não é afetado e permanecerá como era antes da chamada **SortTable** . 
  
## <a name="see-also"></a>Confira também



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

