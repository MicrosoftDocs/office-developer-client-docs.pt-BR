---
title: IOlkApptRebaserEndRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e47d5a8d-6a13-f430-fbfd-00df04b4a006
description: Aguardará compromisso a alteração da base para concluir e recupera os resultados.
ms.openlocfilehash: fd27021ce05b1d5b95fd258e0ee89b5bd4f2c7db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765992"
---
# <a name="iolkapptrebaserendrebaseappointments"></a>IOlkApptRebaser::EndRebaseAppointments

Aguardará compromisso a alteração da base para concluir e recupera os resultados.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkApptRebaser](iolkapptrebaser.md).
  
```cpp
HRESULT EndRebaseAppointments( 
    void *pContext, 
    HRESULT *phResult);
```

## <a name="parameters"></a>Parâmetros

_pContext_
  
> [in] Necessário. Um ponteiro para o contexto obtido de uma chamada para [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).
    
_phResult_
  
> [out] Necessário. Um ponteiro para um **HRESULT** para recuperar o resultado da operação REBASE. 
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.
  
## <a name="see-also"></a>Confira também

- [Sobre alteração de calendários por meio de programação para horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

