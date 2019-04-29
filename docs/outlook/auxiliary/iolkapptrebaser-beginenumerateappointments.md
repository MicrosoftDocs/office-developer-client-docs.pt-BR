---
title: IOlkApptRebaserBeginEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8946703a-aaa8-6b3f-aa68-931365db620d
description: Inicia uma tarefa para enumeração de compromisso em uma pasta de calendário para localizar os compromissos que precisam de alteração de base.
ms.openlocfilehash: cc89b3510f09bb98fd6720cb6d5ab3edeb13eac8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407267"
---
# <a name="iolkapptrebaserbeginenumerateappointments"></a>IOlkApptRebaser::BeginEnumerateAppointments

Inicia uma tarefa para enumeração de compromisso em uma pasta de calendário para localizar os compromissos que precisam de alteração de base.
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkApptRebaser](iolkapptrebaser.md).
  
```cpp
HRESULT BeginEnumerateAppointments( 
    PFNREBASETASKPROGRESS pfnProgress, 
    void **ppContext);
```

## <a name="parameters"></a>Parâmetros

_pfnProgress_
  
> [in] Opcional. Um ponteiro para uma função de progresso da tarefa de alteração da base para receber progresso. **PFNREBASETASKPROGRESS** é definido em tzmovelib.h 
    
_ppContext_
  
> [out] Obrigatório. Um ponteiro para um ponteiro para o contexto retornado. Este contexto será passado para [IOlkApptRebaser:: EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.
  
## <a name="remarks"></a>Comentários

Esta tarefa é executada em um novo segmento.
  
## <a name="see-also"></a>Confira também

- [Sobre a alteração programática da base de calendários para o horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

