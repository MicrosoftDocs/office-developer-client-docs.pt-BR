---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Relata o andamento da enumeração e alteração programática de compromissos.
ms.openlocfilehash: e5df0cd6df10ab86b1a125b9807637438976726f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326450"
---
# <a name="rebasetaskprogress"></a>RebaseTaskProgress

Relata o andamento da enumeração e alteração programática de compromissos.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |tzmovelib.h  <br/> |
|Implementado por:  <br/> |Aplicativos clientes MAPI  <br/> |
|Chamado por:  <br/> |Objeto rebasing do Outlook  <br/> |
|Tipo de ponteiro:  <br/> |**PFNREBASETASKPROGRESS**, conforme definido em tzmovelib.h  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a>Parâmetros

_ulMin_
  
> [in] A extremidade inferior do intervalo de compromissos sendo processados. Geralmente, é zero.
    
_ulMax_
  
> [in] A extremidade superior do intervalo de compromissos sendo processados. Geralmente, é o número de itens na pasta do calendário que está sendo processado.
    
_ulCur_
  
> [in] O item atual sendo processado.
    
_State_
  
> [in] Um valor que indica o status do item que está sendo processado. A enumeração **REBASE_APPT_STATE** é definida em tzmovelib.h.  _State_ é um dos valores a seguir: 
    
   - **REBASE_APPT_STATE_SCANNING_EXAMINING** —Digitalizar e examinar um item. 
    
   - **REBASE_APPT_STATE_SCANNING_FOUND** —Digitalizar e encontrar um item. 
    
   - **REBASE_APPT_STATE_BEGIN** —Corrigir e iniciar um item. 
    
   - **REBASE_APPT_STATE_REBASING** —Corrigir e ajustar um item. 
    
   - **REBASE_APPT_STATE_SENDING** —Corrigir e enviar uma atualização de reunião. 
    
   - **REBASE_APPT_STATE_DONE** —Corrigir e concluir com um item. 
    
_pRowCur_
  
> [in] Um ponteiro para uma estrutura **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** que descreve o item sendo verificado ou corrigido. 
    
## <a name="return-values"></a>Valor de retorno

S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.
  
## <a name="remarks"></a>Comentários

Aplicativos cliente MAPI que usam a interface [IOlkApptRebaser](iolkapptrebaser.md) implementam essa função para acompanhar o processamento de itens. 
  
## <a name="see-also"></a>Confira também

- [Sobre a alteração programática da base de calendários para o horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

