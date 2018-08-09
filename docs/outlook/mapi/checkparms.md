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
ms.openlocfilehash: e7a4fde57515f0b8a41b9acf4adb01dd177a7a19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766283"
---
# <a name="checkparms"></a>CheckParms

  
  
**Aplica-se a**: Outlook 
  
Chama uma função interna para validar os parâmetros de depuração em métodos do provedor de serviço chamados pelo MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços  <br/> |
   
```cpp
HRESULT CheckParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Parâmetros

 _eMethod_
  
> [in] Especifica o enumeração, o método para validar. 
    
 _Primeira_
  
> [in] Ponteiro para o primeiro argumento na pilha.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida.
    
## <a name="remarks"></a>Comentários

Ao contrário de macros [ValidateParms](validateparms.md) e [UlValidateParms](ulvalidateparms.md) , a macro **CheckParms** não realiza uma validação de parâmetro completo. Parâmetros passados entre MAPI e o serviço provedores são consideradas corretas, portanto **CheckParms** executa apenas uma validação de depuração. 
  

