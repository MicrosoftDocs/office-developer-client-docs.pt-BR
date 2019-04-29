---
title: DeinitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeinitMapiUtil
api_type:
- HeaderDef
ms.assetid: e0b8dc9c-cc46-4d27-9497-7a55a0bfdff5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a9654efc34280941cdbc727bce9912a0a39d0fb9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427343"
---
# <a name="deinitmapiutil"></a>DeinitMapiUtil

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Libera funções utilitárias chamadas explicitamente pela função [ScInitMapiUtil](scinitmapiutil.md) ou implicitamente pela função [MAPIInitialize](mapiinitialize.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a>Parâmetros

Nenhum 
  
## <a name="return-value"></a>Valor de retorno

Nenhum 
  
## <a name="remarks"></a>Comentários

As funções de lançamento da função **DeinitMapiUtil** inicializadas com o [ScInitMapiUtil](scinitmapiutil.md) ou o [MAPIInitialize](mapiinitialize.md). 
  
Quando o uso das funções chamadas por **ScInitMapiUtil** estiver concluído, **DeinitMapiUtil** deverá ser explicitamente chamado para liberá-las. Por outro lado, [MAPIUninitialize](mapiuninitialize.md) chama implicitamente **DeinitMapiUtil**. 
  

