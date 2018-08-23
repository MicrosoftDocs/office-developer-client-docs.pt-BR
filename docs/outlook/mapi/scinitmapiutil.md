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
ms.openlocfilehash: 3176280de33bda01bfd09ebaafc31d326d455a3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575032"
---
# <a name="scinitmapiutil"></a>ScInitMapiUtil

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Substitui [MAPIInitialize](mapiinitialize.md) quando somente o utilitário selecionar funções estão sendo usadas. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

As funções **ScInitMapiUtil** e [DeinitMapiUtil](deinitmapiutil.md) cooperam visando chamada e funções de funções, em vez de [MAPIInitialize](mapiinitialize.md), que chama o núcleo bem como utilitário do utilitário select de lançamento. Quando **ScInitMapiUtil** chama as funções do utilitário, ele também inicializa a memória necessária. 
  
Quando o uso das funções que **ScInitMapiUtil** chamou estiver concluído, **DeinitMapiUtil** deve ser chamado explicitamente para liberá-los. Por outro lado, **MAPIInitialize** implicitamente chama **DeinitMapiUtil**. 
  
## <a name="see-also"></a>Confira também



[MAPIUninitialize](mapiuninitialize.md)

