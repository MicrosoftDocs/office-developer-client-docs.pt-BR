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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: a8f17c3cf3d3d00930f87acd004b24f683a3fc8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766563"
---
# <a name="flatentrylist"></a>FLATENTRYLIST

**Aplica-se a**: Outlook 
  
Contém uma matriz de estruturas [FLATENTRY](flatentry.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Macros relacionadas:  <br/> |[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a>Membros

**cEntries**
  
> Contagem de estruturas **FLATENTRY** na matriz descrito pelo membro **abEntries** . 
    
**cbEntries**
  
> Contagem de bytes na matriz descrita por **abEntries**. 
    
**abEntries**
  
> Matriz de bytes que contém uma ou mais estruturas **FLATENTRY** , organizada ponta a ponta. 
    
## <a name="remarks"></a>Coment�rios

Na matriz **abEntries** , cada estrutura **FLATENTRY** é alinhada em um limite naturalmente alinhado. Bytes extras são incluídos como preenchimento para tornar o alinhamento certeza natural entre qualquer duas estruturas **FLATENTRY** . A estrutura **FLATENTRY** primeira na matriz é sempre alinhada corretamente porque o deslocamento do membro **abEntries** é 8. Para calcular o deslocamento da próxima estrutura, use o tamanho da primeira entrada arredondado para cima até o próximo múltiplo de 4. Use a macro [CbFLATENTRY](cbflatentry.md) para calcular o tamanho de uma estrutura **FLATENTRY** . 
  
Por exemplo, a estrutura **FLATENTRY** segunda é iniciado em um deslocamento que consiste o deslocamento da primeira entrada mais o comprimento da primeira entrada arredondado para o próximo de quatro bytes. O comprimento da primeira entrada é o comprimento da sua lista de membros **cb** mais o comprimento do seu membro **abEntry** . 
  
O exemplo de código a seguir indica como compute deslocamentos em uma estrutura **FLATENTRYLIST** . Suponha que _lpFlatEntry_ é um ponteiro para a estrutura primeiro na lista. 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a>Confira também

- [FLATENTRY](flatentry.md)
- [Propriedade canônico de PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)
- [Estruturas MAPI](mapi-structures.md)

