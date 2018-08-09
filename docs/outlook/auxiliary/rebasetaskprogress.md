---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Relatórios de progresso para enumeração e a alteração da Base de compromissos.
ms.openlocfilehash: 4219ab1d59b596bebbe3ced03651716b04b51f81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766077"
---
# <a name="rebasetaskprogress"></a>RebaseTaskProgress

Relatórios de progresso para enumeração e a alteração da Base de compromissos.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |tzmovelib.h  <br/> |
|Implementada por:  <br/> |Aplicativos de cliente MAPI  <br/> |
|Chamado pelo:  <br/> |REBASE de objeto do Outlook  <br/> |
|Tipo de ponteiro:  <br/> |**PFNREBASETASKPROGRESS** conforme definido em tzmovelib.h  <br/> |
   
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
  
> [in] O término de baixo do intervalo de compromissos que estão sendo processadas. Normalmente é zero.
    
_ulMax_
  
> [in] High-end do intervalo de compromissos que estão sendo processadas. Geralmente é o número de itens na pasta de calendário que estão sendo processadas.
    
_ulCur_
  
> [in] O item atual que está sendo processado.
    
_Estado_
  
> [in] Um valor que indica o status do item que estão sendo processado. A enumeração **REBASE_APPT_STATE** é definida em tzmovelib.h.  _Estado_ é um dos seguintes valores: 
    
   - **REBASE_APPT_STATE_SCANNING_EXAMINING** — digitalização e examinando a um item. 
    
   - **REBASE_APPT_STATE_SCANNING_FOUND** — examinando e encontrado um item. 
    
   - **REBASE_APPT_STATE_BEGIN** — corrigindo e iniciando a um item. 
    
   - **REBASE_APPT_STATE_REBASING** — corrigindo e ajustando um item. 
    
   - **REBASE_APPT_STATE_SENDING** — corrigindo e envio de uma atualização de reunião. 
    
   - **REBASE_APPT_STATE_DONE** — corrigindo e concluído com um item. 
    
_pRowCur_
  
> [in] Um ponteiro para uma estrutura **[SRow](http://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** que descreve o item que estão sendo verificados ou fixa. 
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.
  
## <a name="remarks"></a>Comentários

Aplicativos de cliente MAPI que usam a interface [IOlkApptRebaser](iolkapptrebaser.md) implementam esta função para controlar o processamento do item. 
  
## <a name="see-also"></a>Confira também

- [Sobre alteração de calendários por meio de programação para horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

