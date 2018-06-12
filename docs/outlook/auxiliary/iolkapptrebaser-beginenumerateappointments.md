---
title: IOlkApptRebaserBeginEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8946703a-aaa8-6b3f-aa68-931365db620d
description: Inicia uma tarefa a enumeração de compromisso em uma pasta de calendário para encontrar os compromissos que precisam a alteração da base.
ms.openlocfilehash: 2ad26692483d87166a538ec2f04d3fc13b9ea930
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765977"
---
# <a name="iolkapptrebaserbeginenumerateappointments"></a>IOlkApptRebaser::BeginEnumerateAppointments

Inicia uma tarefa a enumeração de compromisso em uma pasta de calendário para encontrar os compromissos que precisam a alteração da base.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkApptRebaser](iolkapptrebaser.md).
  
```cpp
HRESULT BeginEnumerateAppointments( 
    PFNREBASETASKPROGRESS pfnProgress, 
    void **ppContext);
```

## <a name="parameters"></a>Par�metros

_pfnProgress_
  
> [in] Opcional. Um ponteiro para uma função de andamento de tarefa alterar para receber o progresso. **PFNREBASETASKPROGRESS** é definido em tzmovelib.h. 
    
_ppContext_
  
> [out] Necessário. Um ponteiro para um ponteiro para o contexto retornado. Nesse contexto será transmitido ao [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.
  
## <a name="remarks"></a>Coment�rios

Esta tarefa é executada em um novo segmento.
  
## <a name="see-also"></a>Confira também

- [Sobre alteração de calendários por meio de programação para horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

