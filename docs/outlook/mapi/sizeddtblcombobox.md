---
title: SizedDtblComboBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblComboBox
api_type:
- COM
ms.assetid: 1e5ea9f2-1029-4584-845a-890d3e956036
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8861c8f86eaab6defb270b673e0ee200446aedb3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416262"
---
# <a name="sizeddtblcombobox"></a>SizedDtblComboBox
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria uma estrutura nomeada que inclui uma [estrutura DTBLCOMBOBOX](dtblcombobox.md) para descrever um controle caixa de combinação e o número máximo de caracteres que podem ser inseridos no controle de edição associado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada:  <br/> |**DTBLCOMBOBOX** <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a>Parâmetros

_n_
  
> Número de caracteres que podem ser inseridos no controle de edição da caixa de combinação. 
    
_u_
  
> Nome da nova estrutura.
    
## <a name="remarks"></a>Comentários

A macro **SizedDtblComboBox** permite definir uma caixa de combinação quando o comprimento da cadeia de caracteres habilitada for conhecido. A nova estrutura é criada com os seguintes membros: 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

Para usar um ponteiro para a estrutura resultante da macro **SizedDtblComboBox** como um ponteiro de **estrutura DTBLCOMBOBOX,** execute a seguinte projeção: 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a>Confira também

- [DTBLCOMBOBOX](dtblcombobox.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)

