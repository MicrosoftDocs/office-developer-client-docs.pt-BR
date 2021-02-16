---
title: CheckParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParameters
api_type:
- COM
ms.assetid: ba33866a-c9c4-454a-9549-72455c61ee97
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a922b8bb21bfd534935d4d1706a6ccfd15c2da5c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433392"
---
# <a name="checkparameters"></a>CheckParameters

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Chama uma função interna para validar parâmetros de depuração em métodos de provedor de serviços chamados por MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços  <br/> |
   
```cpp
HRESULT CheckParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Parâmetros

 _eMethod_
  
> [in] Especifica, por enumeração, o método a ser validado. 
    
 _Primeira_
  
> [in] Ponteiro para o primeiro argumento na pilha.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida.
    
## <a name="remarks"></a>Comentários

A **macro CheckParameters** foi sobressalvada pela macro [CheckParms.](checkparms.md) **CheckParms é** recomendado em todas as plataformas. 
  

