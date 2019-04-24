---
title: CheckParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CheckParms
api_type:
- COM
ms.assetid: 328f12f0-e4e7-407f-8eb8-0d4bf543962d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ffa1b596b2f60bce35f24df8a20326502be8165a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331798"
---
# <a name="checkparms"></a>CheckParms

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Chama uma função interna para validar parâmetros de depuração nos métodos de provedor de serviços chamados por MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Parâmetros

 _eMethod_
  
> no Especifica, por enumeração, o método a ser validado. 
    
 _Primeira_
  
> no Ponteiro para o primeiro argumento na pilha.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida.
    
## <a name="remarks"></a>Comentários

Ao contrário das macros [ValidateParms](validateparms.md) e [UlValidateParms](ulvalidateparms.md) , a macro **CheckParms** não realiza uma validação de parâmetro completa. Os parâmetros passados entre MAPI e provedores de serviço são considerados corretos, portanto, **CheckParms** executa apenas uma validação de depuração. 
  

