---
title: MTSID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MTSID
api_type:
- COM
ms.assetid: 3d9bc643-332f-4c8e-83e6-ce9b15711945
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 59e9cf23aed2a389384318468c3853cd41c9ec1e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585679"
---
# <a name="mtsid"></a>MTSID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um identificador de entrada x. 400 mensagem transporte MTS (sistema). 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Macros relacionadas:  <br/> |[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a>Members

 **cb**
  
> Contagem de bytes na matriz descrito pelo membro **abEntry** . 
    
 **abEntry**
  
> Matriz de bytes que contém os dados do identificador de entrada MTS.
    
## <a name="remarks"></a>Comentários

A estrutura **MTSID** é usada somente para mapeamentos de x. 400 dos identificadores de entrada MAPI. Ela corresponde à estrutura de MAPI [FLATENTRY](flatentry.md) . 
  
Um identificador MTS tem o mesmo formato apresentado um identificador de entrada MAPI ou um valor de propriedade binária. Identificadores MTS podem ser particularmente útil para cancelamento de mensagens adiadas. 
  
## <a name="see-also"></a>Confira também



[FLATENTRY](flatentry.md)
  
[FLATMTSIDLIST](flatmtsidlist.md)


[Estruturas MAPI](mapi-structures.md)

