---
title: IOlkApptRebaserEndEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bc4506c7-7a4f-940d-d0a6-e0fab4561a88
description: Aguarda a conclusão da enumeração de compromissos em uma pasta de calendário e retorna uma lista de compromissos que precisam de alteração programática.
ms.openlocfilehash: 5be6fd9ce33374725b36429cd0fbc717776c9ab9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392015"
---
# <a name="iolkapptrebaserendenumerateappointments"></a>IOlkApptRebaser::EndEnumerateAppointments

Aguarda a conclusão da enumeração de compromissos em uma pasta de calendário e retorna uma lista de compromissos que precisam de alteração programática.
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkApptRebaser](iolkapptrebaser.md).
  
```cpp
HRESULT EndEnumerateAppointments( 
    void *pContext, 
    HRESULT *phResult, 
    MAPIERROR **ppError, 
    SRowSet **ppRows);
```

## <a name="parameters"></a>Parâmetros

_pContext_
  
> [in] Obrigatório. Um ponteiro para o contexto obtido em uma chamada anterior para [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md).
    
_phResult_
  
> [out] Obrigatório. Um ponteiro para um **HRESULT** para recuperar os resultados da operação de enumeração. 
    
_ppError_
  
> [out] Opcional. Um ponteiro para uma estrutura **MAPIERROR** para recuperar informações sobre erros estendidas. 
    
_ppRows_
  
> [out] Obrigatório. Um ponteiro para uma estrutura [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) que descreve os compromissos que precisam de alteração programática. Essa estrutura geralmente é passada para [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).
    
## <a name="return-values"></a>Valor de retorno

S_OK se a chamada foi bem-sucedida. Caso contrário, um código de erro.
  
## <a name="see-also"></a>Confira também

- [Sobre a alteração programática da base de calendários para o horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

