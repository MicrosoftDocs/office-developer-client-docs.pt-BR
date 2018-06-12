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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: ae6f7d7066638ef1b149d3e411443384d531184d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766374"
---
# <a name="deinitmapiutil"></a>DeinitMapiUtil

  
  
**Aplica-se a**: Outlook 
  
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

None 
  
## <a name="return-value"></a>Valor retornado

None 
  
## <a name="remarks"></a>Comentários

A função **DeinitMapiUtil** release funções inicializadas com [ScInitMapiUtil](scinitmapiutil.md) ou [MAPIInitialize](mapiinitialize.md). 
  
Quando o uso das funções chamado pelo **ScInitMapiUtil** estiver concluído, **DeinitMapiUtil** deve ser chamado explicitamente para liberá-los. Por outro lado, [MAPIUninitialize](mapiuninitialize.md) implicitamente chama **DeinitMapiUtil**. 
  

