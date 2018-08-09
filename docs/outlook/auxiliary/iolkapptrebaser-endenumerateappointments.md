---
title: IOlkApptRebaserEndEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bc4506c7-7a4f-940d-d0a6-e0fab4561a88
description: Aguardará enumeração de compromisso em uma pasta de calendário para a conclusão e retorna uma lista de compromissos essa necessidade alteração da base.
ms.openlocfilehash: d7d29a88114d7b3973b8f04e924dc1dd8489a097
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765994"
---
# <a name="iolkapptrebaserendenumerateappointments"></a>IOlkApptRebaser::EndEnumerateAppointments

Aguardará enumeração de compromisso em uma pasta de calendário para a conclusão e retorna uma lista de compromissos essa necessidade alteração da base.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkApptRebaser](iolkapptrebaser.md).
  
```cpp
HRESULT EndEnumerateAppointments( 
    void *pContext, 
    HRESULT *phResult, 
    MAPIERROR **ppError, 
    SRowSet **ppRows);
```

## <a name="parameters"></a>Parâmetros

_pContext_
  
> [in] Necessário. Um ponteiro para o contexto obtido de uma chamada anterior ao [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md).
    
_phResult_
  
> [out] Necessário. Um ponteiro para um **HRESULT** para recuperar os resultados da operação de enumeração. 
    
_ppError_
  
> [out] Opcional. Um ponteiro para um ponteiro para uma estrutura **MAPIERROR** para recuperar informações de erro estendidas. 
    
_ppRows_
  
> [out] Necessário. Um ponteiro para um ponteiro para uma estrutura de [SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) que descreve os compromissos que precisam a alteração da base. Essa estrutura geralmente será transmitida ao [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.
  
## <a name="see-also"></a>Confira também

- [Sobre alteração de calendários por meio de programação para horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

