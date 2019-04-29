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
ms.openlocfilehash: bd9bfe4d1411b84a7811235aa68728afaefe64ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439216"
---
# <a name="flatmtsidlist"></a>FLATMTSIDLIST

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma matriz de estruturas [MTSID](mtsid.md) , cada uma contendo um identificador de entrada do sistema de transporte de mensagens (MTS) X. 400. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
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
  
> Contagem de estruturas **MTSID** na matriz descrita pelo membro **abMTSIDs** . 
    
 **cbMTSIDs**
  
> Contagem de bytes na matriz descrita por **abMTSIDs**.
    
 **abMTSIDs**
  
> Matriz de bytes que contém uma ou mais estruturas **MTSID** . 
    
## <a name="remarks"></a>Comentários

O uso da estrutura **FLATMTSIDLIST** em uma mensagem X. 400 corresponde ao uso da estrutura [FLATENTRYLIST](flatentrylist.md) em mensagens MAPI. MAPI usa estruturas **FLATMTSIDLIST** para manter as propriedades X. 400 durante o tratamento de mensagens. Os provedores de serviços usam estruturas **FLATMTSIDLIST** ao lidar com as mensagens X. 400 de entrada e de saída. 
  
Na matriz **abMTSIDs** , cada estrutura **MTSID** é alinhada em um limite naturalmente alinhado. Bytes extras são incluídos como enchimento para garantir o alinhamento natural entre duas estruturas **MTSID** . A primeira estrutura **MTSID** na matriz é sempre alinhada corretamente porque o deslocamento do membro **abMTSIDs** é 8. Para calcular o deslocamento da próxima estrutura, use o tamanho da primeira entrada arredondado para o próximo múltiplo de 4. Use a macro [CbNewMTSID](cbnewmtsid.md) para calcular o tamanho de uma estrutura **MTSID** . 
  
## <a name="see-also"></a>Confira também



[CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)
  
[FLATENTRYLIST](flatentrylist.md)
  
[MTSID](mtsid.md)


[Estruturas MAPI](mapi-structures.md)

