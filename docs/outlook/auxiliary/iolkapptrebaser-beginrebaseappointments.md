---
title: IOlkApptRebaserBeginRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed50422e-9edf-4b73-1789-340b70532621
description: Inicia uma tarefa a alteração da base compromisso fornecida uma lista de compromissos, normalmente obtido da IOlkApptRebaser::EndEnumerateAppointments.
ms.openlocfilehash: 2becb305eebe448e2adecf91c2a111f86d97fe50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765996"
---
# <a name="iolkapptrebaserbeginrebaseappointments"></a>IOlkApptRebaser::BeginRebaseAppointments

Inicia uma tarefa a alteração da compromisso base fornecida uma lista de compromissos, normalmente obtido da [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkApptRebaser](iolkapptrebaser.md).
  
```cpp
HRESULT BeginRebaseAppointments( 
    const SRowSet *pRows, 
    PFNREBASETASKPROGRESS pfnProgress, 
    PFNREBASETASKCOMPLETE pfnComplete, 
    void **ppContext);
```

## <a name="parameters"></a>Parâmetros

_pRows_
  
> [in] Necessário. Um ponteiro para uma estrutura de [SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) que descreve os compromissos que precisam a alteração da base. Essa estrutura é obtida geralmente uma chamada anterior ao [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).
    
_pfnProgress_
  
> [in] Opcional. Um ponteiro para uma função de andamento de tarefa alterar para receber o progresso. **PFNREBASETASKPROGRESS** é definido em tzmovelib.h. 
    
_pfnComplete_
  
> [out] Opcional. Um ponteiro para uma função de conclusão de tarefa alterar para receber uma notificação de conclusão de alterar. **PFNREBASETASKCOMPLETE** é definido em tzmovelib.h. 
    
_ppContext_
  
> [out] Necessário. Um ponteiro para um ponteiro para o contexto retornado. Nesse contexto geralmente será transmitido ao [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md).
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.
  
## <a name="remarks"></a>Comentários

Esta tarefa é executada em um novo segmento.
  
## <a name="see-also"></a>Confira também

- [Sobre alteração de calendários por meio de programação para horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

