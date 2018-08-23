---
title: SizedENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedENTRYID
api_type:
- COM
ms.assetid: 491170af-db35-4d7e-a912-44ffe8c7506b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d797acdbf2abfb88151d69d0c93e743f07afc5c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563867"
---
# <a name="sizedentryid"></a>SizedENTRYID

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria uma estrutura [ENTRYID](entryid.md) nomeada que contém um membro **ab** de um tamanho especificado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada:  <br/> |**ENTRYID** <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a>Parâmetros

__cb_
  
> Contagem de bytes no membro **ab** da nova estrutura. 
    
__nome_
  
> Nome para a nova estrutura.
    
## <a name="remarks"></a>Comentários

A macro **SizedENTRYID** permite definir um identificador de entrada após os requisitos de tamanho da matriz são conhecidos. Use essa macro para criar um identificador de entrada com limites explícitos. 
  
Para usar a nova estrutura que é resultado da macro **SizedENTRYID** como um ponteiro para uma estrutura **ENTRYID** , execute a seguinte projeção: 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a>Confira também

- [ENTRYID](entryid.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)

