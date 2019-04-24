---
title: IOlkApptRebaserEndRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e47d5a8d-6a13-f430-fbfd-00df04b4a006
description: Aguarda a alteração da base do compromisso para concluir e recupera os resultados.
ms.openlocfilehash: a6e62cff9efea1fc7079d04bc9b032b5637f8847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321886"
---
# <a name="iolkapptrebaserendrebaseappointments"></a>IOlkApptRebaser::EndRebaseAppointments

Aguarda a alteração da base do compromisso para concluir e recupera os resultados.
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkApptRebaser](iolkapptrebaser.md).
  
```cpp
HRESULT EndRebaseAppointments( 
    void *pContext, 
    HRESULT *phResult);
```

## <a name="parameters"></a>Parâmetros

_pContext_
  
> [in] Obrigatório. Um ponteiro para o contexto obtido de uma chamada para [IOlkApptRebaser:: BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).
    
_phResult_
  
> [out] Obrigatório. Um ponteiro para um **HRESULT** para recuperar o resultado da operação de alteração da base. 
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada foi bem-sucedida. Caso contrário, um código de erro.
  
## <a name="see-also"></a>Confira também

- [Sobre a alteração programática da base de calendários para o horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

