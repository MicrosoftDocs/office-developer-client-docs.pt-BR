---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: Conclusão de relatórios para a alteração da Base de compromissos.
ms.openlocfilehash: 735d875b4151c86103a1ac0378bd33b84de64997
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766081"
---
# <a name="rebasetaskcomplete"></a>RebaseTaskComplete

Conclusão de relatórios para a alteração da Base de compromissos.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |tzmovelib.h  <br/> |
|Implementada por:  <br/> |Aplicativos de cliente MAPI  <br/> |
|Chamado pelo:  <br/> |REBASE de objeto do Outlook  <br/> |
|Tipo de ponteiro:  <br/> |**PFNREBASETASKCOMPLETE** conforme definido em tzmovelib.h  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskComplete(  
    ULONG ulRowIndex, 
    const SRow* pRowCur, 
    HRESULT hrResult, 
    BOOL fModified, 
    BOOL fSentUpdate, 
    const MAPIERROR* pError); 

```

## <a name="parameters"></a>Par�metros

_ulRowIndex_
  
> [in] Na linha que foi processada. Esse índice refere-se à estrutura **[SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** passada para [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).
    
_pRowCur_
  
> in] um ponteiro para uma estrutura **[SRow](http://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** descrevendo o item que foi processado. 
    
_hrResult_
  
> [in] Um **HRESULT** indicando o resultado da operação REBASE. 
    
_fModified_
  
> [in] Especifica se o item foi modificado.
    
_fSentUpdate_
  
> [in] Especifica se uma reunião atualizar a mensagem foi enviada. 
    
_pError_
  
> [in] Um ponteiro para uma estrutura **MAPIERROR** com informações de erro estendidas. 
    
## <a name="return-values"></a>Valores de retorno

S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.
  
## <a name="remarks"></a>Coment�rios

Aplicativos de cliente MAPI que usam a interface [IOlkApptRebaser](iolkapptrebaser.md) implementam esta função para controlar a conclusão das atualizações de item. 
  
## <a name="see-also"></a>Confira também

- [Sobre alteração de calendários por meio de programação para horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

