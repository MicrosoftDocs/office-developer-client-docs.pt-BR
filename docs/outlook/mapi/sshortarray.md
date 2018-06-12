---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 59911531b6d8f9c094ef8563510aaa176e3a63b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770502"
---
# <a name="sshortarray"></a>SShortArray

  
  
**Aplica-se a**: Outlook 
  
Contém uma matriz de valores de inteiro não assinado que são usadas para descrever uma propriedade do tipo PT_MV_SHORT.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a>Membros

 **cValues**
  
> Contagem de valores na matriz apontado pelo membro **lpi** . 
    
 **lpi**
  
> Ponteiro para uma matriz de valores de inteiro não assinado.
    
## <a name="remarks"></a>Coment�rios

Para obter mais informações sobre PT_MV_SHORT e outros tipos de propriedade, consulte [Tipos de propriedade](property-types.md). 
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)

