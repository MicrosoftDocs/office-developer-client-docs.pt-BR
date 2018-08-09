---
title: FLATMTSIDLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATMTSIDLIST
api_type:
- COM
ms.assetid: b66c2815-72bc-4535-b34c-899bb830f29e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ea841ef4bc551581fb2d9ca90201b4615e67f134
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766567"
---
# <a name="flatmtsidlist"></a>FLATMTSIDLIST

  
  
**Aplica-se a**: Outlook 
  
Contém uma matriz de estruturas [MTSID](mtsid.md) , cada um deles contém um identificador de entrada x. 400 mensagem transporte MTS (sistema). 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Macros relacionadas:  <br/> |[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMTSIDs;
  ULONG cbMTSIDs;
  BYTE abMTSIDs[MAPI_DIM];
} FLATMTSIDLIST, FAR *LPFLATMTSIDLIST;

```

## <a name="members"></a>Members

 **cMTSIDs**
  
> Contagem de estruturas **MTSID** na matriz descrito pelo membro **abMTSIDs** . 
    
 **cbMTSIDs**
  
> Contagem de bytes na matriz descrita por **abMTSIDs**.
    
 **abMTSIDs**
  
> Matriz de bytes que contém uma ou mais estruturas **MTSID** . 
    
## <a name="remarks"></a>Comentários

Uso da estrutura **FLATMTSIDLIST** em x. 400 mensagens corresponde ao uso da estrutura [FLATENTRYLIST](flatentrylist.md) em mensagens de MAPI. MAPI usa estruturas **FLATMTSIDLIST** para manter as propriedades de x. 400 durante o tratamento de mensagens. Provedores de serviços usam estruturas **FLATMTSIDLIST** quando lidando com as mensagens de x. 400 de entrada e saídas. 
  
Na matriz **abMTSIDs** , cada estrutura **MTSID** é alinhada em um limite naturalmente alinhado. Bytes extras são incluídos como preenchimento para tornar o alinhamento certeza natural entre qualquer duas estruturas **MTSID** . A estrutura **MTSID** primeira na matriz é sempre alinhada corretamente porque o deslocamento do membro **abMTSIDs** é 8. Para calcular o deslocamento da próxima estrutura, use o tamanho da primeira entrada arredondado para cima até o próximo múltiplo de 4. Use a macro [CbNewMTSID](cbnewmtsid.md) para calcular o tamanho de uma estrutura **MTSID** . 
  
## <a name="see-also"></a>Confira também



[CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)
  
[FLATENTRYLIST](flatentrylist.md)
  
[MTSID](mtsid.md)


[Estruturas MAPI](mapi-structures.md)

