---
title: IOlkApptRebaserBeginRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed50422e-9edf-4b73-1789-340b70532621
description: Inicia uma tarefa para alterar a base de compromisso, dada uma lista de compromissos, geralmente obtida de IOlkApptRebaser::EndEnumerateAppointments.
ms.openlocfilehash: f0f2377f30de7688aaa4196e3a046c664c2128aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321907"
---
# <a name="iolkapptrebaserbeginrebaseappointments"></a>IOlkApptRebaser::BeginRebaseAppointments

Inicia uma tarefa para alterar a base de compromisso, dada uma lista de compromissos, geralmente obtida de [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkApptRebaser](iolkapptrebaser.md).
  
```cpp
HRESULT BeginRebaseAppointments( 
    const SRowSet *pRows, 
    PFNREBASETASKPROGRESS pfnProgress, 
    PFNREBASETASKCOMPLETE pfnComplete, 
    void **ppContext);
```

## <a name="parameters"></a>Parâmetros

_pRows_
  
> [in] Obrigatório. Um ponteiro para uma estrutura [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) que descreve os compromissos que precisam de alteração programática. Essa estrutura é obtida em uma chamada anterior para [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).
    
_pfnProgress_
  
> [in] Opcional. Um ponteiro para uma função de progresso da tarefa de alteração da base para receber progresso. **PFNREBASETASKPROGRESS** é definido em tzmovelib.h 
    
_pfnComplete_
  
> [out] Opcional. Um ponteiro para uma função de conclusão de tarefa de alteração da base para receber notificação de conclusão de alteração da base. **PFNREBASETASKCOMPLETE** é definido em tzmovelib.h 
    
_ppContext_
  
> [out] Obrigatório. Um ponteiro para um ponteiro para o contexto retornado. Essa estrutura geralmente é passada para [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md).
    
## <a name="return-values"></a>Valor de retorno

S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.
  
## <a name="remarks"></a>Comentários

Esta tarefa é executada em um novo segmento.
  
## <a name="see-also"></a>Confira também

- [Sobre a alteração programática da base de calendários para o horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

