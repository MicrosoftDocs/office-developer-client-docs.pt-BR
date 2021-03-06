---
title: ScInitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ScInitMapiUtil
api_type:
- HeaderDef
ms.assetid: d83b8ea8-a3b8-4038-a226-de1869c5d722
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 090a73ed908d2a647d00de27b93538a77766c258
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420588"
---
# <a name="scinitmapiutil"></a>ScInitMapiUtil

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Substitui [MAPIInitialize](mapiinitialize.md) quando apenas funções utilitais selecionadas estão sendo usadas. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos do cliente  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

As funções **ScInitMapiUtil** e [DeinitMapiUtil](deinitmapiutil.md) cooperam para chamar e liberar funções utilitais selecionadas, em oposição a [MAPIInitialize](mapiinitialize.md), que chama o núcleo, bem como funções de utilitário. Quando **ScInitMapiUtil** chama funções de utilitário, ele também inicializa a memória necessária. 
  
Quando o uso das funções que **ScInitMapiUtil** chamou está concluído, **DeinitMapiUtil** deve ser chamado explicitamente para liberá-las. Por outro lado, **MAPIInitialize** implicitamente chama **DeinitMapiUtil**. 
  
## <a name="see-also"></a>Confira também



[MAPIUninitialize](mapiuninitialize.md)

