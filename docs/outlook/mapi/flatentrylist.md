---
title: FLATENTRYLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRYLIST
api_type:
- COM
ms.assetid: b465d015-9b62-4986-b0df-118121f60602
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bc511ea4b3ec4eea9e38f744bcb8f277108085cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413854"
---
# <a name="flatentrylist"></a>FLATENTRYLIST

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma matriz de estruturas [FLATENTRY](flatentry.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Macros relacionadas:  <br/> |[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a>Members

**cEntries**
  
> Contagem de estruturas **FLATENTRY** na matriz descrita pelo membro **abEntries** . 
    
**cbEntries**
  
> Contagem de bytes na matriz descrita por **abEntries**. 
    
**abEntries**
  
> Matriz de bytes que contém uma ou mais estruturas **FLATENTRY** , organizadas de ponta a ponta. 
    
## <a name="remarks"></a>Comentários

Na matriz **abEntries** , cada estrutura **FLATENTRY** é alinhada em um limite naturalmente alinhado. Bytes extras são incluídos como enchimento para garantir o alinhamento natural entre duas estruturas **FLATENTRY** . A primeira estrutura **FLATENTRY** na matriz é sempre alinhada corretamente porque o deslocamento do membro **abEntries** é 8. Para calcular o deslocamento da próxima estrutura, use o tamanho da primeira entrada arredondado para o próximo múltiplo de 4. Use a macro [CbFLATENTRY](cbflatentry.md) para calcular o tamanho de uma estrutura **FLATENTRY** . 
  
Por exemplo, a segunda estrutura **FLATENTRY** começa em um deslocamento que consiste no deslocamento da primeira entrada, além do comprimento da primeira entrada arredondada para os próximos quatro bytes. O comprimento da primeira entrada é o comprimento do seu membro **CB** mais o comprimento de seu membro **abEntry** . 
  
O exemplo de código a seguir indica como computar deslocamentos em uma estrutura **FLATENTRYLIST** . Suponha que _lpFlatEntry_ é um ponteiro para a primeira estrutura na lista. 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a>Confira também

- [FLATENTRY](flatentry.md)
- [Propriedade canônica PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)
- [Estruturas MAPI](mapi-structures.md)

