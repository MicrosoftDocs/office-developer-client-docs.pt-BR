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
ms.openlocfilehash: 88cf91330dea82dda490b81cc8de6fea0504baf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282681"
---
# <a name="sizedentryid"></a>SizedENTRYID

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria uma estrutura [EntryID](entryid.md) nomeada que contém um membro **AB** de um tamanho especificado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Estrutura relacionada:  <br/> |**ENTRYID** <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a>Parâmetros

__CB_
  
> Contagem de bytes no membro **AB** da nova estrutura. 
    
__nome_
  
> Nome da nova estrutura.
    
## <a name="remarks"></a>Comentários

A macro **SizedENTRYID** permite que você defina um identificador de entrada após os requisitos de comprimento de matriz serem conhecidos. Use essa macro para criar um identificador de entrada com limites explícitos. 
  
Para usar a nova estrutura que resulta da macro **SizedENTRYID** como um ponteiro para uma estrutura **EntryID** , execute a seguinte conversão: 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a>Confira também

- [ENTRYID](entryid.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)

