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
ms.openlocfilehash: e84dbc0976f5c438a7e0b5fd7cddcbf1c0659f40
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574794"
---
# <a name="deinitmapiutil"></a>DeinitMapiUtil

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Libera funções do utilitário chamadas explicitamente pela função [ScInitMapiUtil](scinitmapiutil.md) ou implicitamente pela função [MAPIInitialize](mapiinitialize.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a>Parâmetros

Nenhum 
  
## <a name="return-value"></a>Valor retornado

None 
  
## <a name="remarks"></a>Comentários

A função **DeinitMapiUtil** release funções inicializadas com [ScInitMapiUtil](scinitmapiutil.md) ou [MAPIInitialize](mapiinitialize.md). 
  
Quando o uso das funções chamado pelo **ScInitMapiUtil** estiver concluído, **DeinitMapiUtil** deve ser chamado explicitamente para liberá-los. Por outro lado, [MAPIUninitialize](mapiuninitialize.md) implicitamente chama **DeinitMapiUtil**. 
  

