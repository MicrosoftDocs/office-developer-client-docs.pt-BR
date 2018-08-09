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
ms.openlocfilehash: 814cfeab61854469f460cc38f927b0e3723f6f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770418"
---
# <a name="sizedentryid"></a>SizedENTRYID

**Aplica-se a**: Outlook 
  
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

