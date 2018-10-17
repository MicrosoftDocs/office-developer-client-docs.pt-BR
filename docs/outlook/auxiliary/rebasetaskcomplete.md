---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: Relata a conclusão da alteração programática de compromissos.
ms.openlocfilehash: 9fab0d06bf0b9856b9a968f5c0db1bb15b0fe0bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388914"
---
# <a name="rebasetaskcomplete"></a>RebaseTaskComplete

Relata a conclusão da alteração programática de compromissos.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |tzmovelib.h  <br/> |
|Implementado por:  <br/> |Aplicativos clientes MAPI  <br/> |
|Chamado por:  <br/> |Objeto rebasing do Outlook  <br/> |
|Tipo de ponteiro:  <br/> |**PFNREBASETASKCOMPLETE**, conforme definido em tzmovelib.h  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskComplete(  
    ULONG ulRowIndex, 
    const SRow* pRowCur, 
    HRESULT hrResult, 
    BOOL fModified, 
    BOOL fSentUpdate, 
    const MAPIERROR* pError); 

```

## <a name="parameters"></a>Parâmetros

_ulRowIndex_
  
> [in] A linha que foi processada. Este índice refere-se à estrutura **[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** passada para [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).
    
_pRowCur_
  
> in] Um ponteiro para uma estrutura **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** que descreve o item processado. 
    
_hrResult_
  
> [in] Um **HRESULT** que indica o resultado da operação de alteração programática. 
    
_fModified_
  
> [in] Especifica se o item foi modificado.
    
_fSentUpdate_
  
> [em] Especifica se uma mensagem de atualização da reunião foi enviada. 
    
_pError_
  
> [in] Um ponteiro para uma estrutura **MAPIERROR** com informações sobre erros estendidas. 
    
## <a name="return-values"></a>Valor de retorno

S_OK se a chamada foi bem-sucedida. Caso contrário, um código de erro.
  
## <a name="remarks"></a>Comentários

Aplicativos cliente MAPI que usam a interface [IOlkApptRebaser](iolkapptrebaser.md) implementam essa função para controlar a conclusão de atualizações do item. 
  
## <a name="see-also"></a>Confira também

- [Sobre a alteração programática da base de calendários para o horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

