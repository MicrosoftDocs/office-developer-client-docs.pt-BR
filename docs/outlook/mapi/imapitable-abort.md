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
ms.openlocfilehash: 74c307fca27f1adec18d236792f8a58d97e33ec5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406147"
---
# <a name="imapitableabort"></a>IMAPITable::Abort

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Interrompe qualquer operação assíncrona em andamento para a tabela.
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a>Parâmetros

Nenhum
  
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Uma ou mais operações assíncronas foram interrompidas.
    
MAPI_E_UNABLE_TO_ABORT 
  
> Uma operação assíncrona está em andamento e não pode ser interrompida ou já foi concluída.
    
## <a name="remarks"></a>Comentários

O **método IMAPITable::Abort** interrompe qualquer operação assíncrona que está em andamento. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para descobrir se uma operação assíncrona está em andamento, chame o método [IMAPITable::GetStatus.](imapitable-getstatus.md) 
  
Se **Abort** interromper o processamento de uma chamada para o método [IMAPITable::Restrict,](imapitable-restrict.md) o estado da tabela será como estava no momento em que a chamada **abort** for processada. 
  
Se **Abort** interromper o processamento de uma chamada para o método [IMAPITable::SortTable,](imapitable-sorttable.md) a ordem de classificação da tabela não será afetada e permanecerá como era antes da chamada **sorttable.** 
  
## <a name="see-also"></a>Confira também



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

