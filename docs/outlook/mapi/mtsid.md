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
ms.openlocfilehash: 96da91acec741322e6c07c64555171d35f0f7e00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435170"
---
# <a name="mtsid"></a>MTSID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um identificador de entrada MTS (sistema de transporte de mensagens) X. 400. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
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
  
> Contagem de bytes na matriz descrita pelo membro **abEntry** . 
    
 **abEntry**
  
> Matriz de bytes que contém os dados do identificador de entrada MTS.
    
## <a name="remarks"></a>Comentários

A estrutura **MTSID** é usada apenas para mapeamentos X. 400 de identificadores de entrada MAPI. Ela corresponde à estrutura [FLATENTRY](flatentry.md) MAPI. 
  
Um identificador MTS tem o mesmo formato que um identificador de entrada MAPI ou um valor de propriedade binária. Os identificadores MTS podem ser particularmente úteis para cancelar mensagens adiadas. 
  
## <a name="see-also"></a>Confira também



[FLATENTRY](flatentry.md)
  
[FLATMTSIDLIST](flatmtsidlist.md)


[Estruturas MAPI](mapi-structures.md)

