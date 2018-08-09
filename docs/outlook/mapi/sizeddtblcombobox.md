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
ms.openlocfilehash: fea2b496a34d7aa7f9469158fae14daf6a770608
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770424"
---
# <a name="sizeddtblcombobox"></a>SizedDtblComboBox
 
**Aplica-se a**: Outlook 
  
Cria uma estrutura nomeada que inclui uma estrutura [DTBLCOMBOBOX](dtblcombobox.md) para descrever um controle de caixa de combinação e o número máximo de caracteres que podem ser inseridos no controle de edição associado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada:  <br/> |**DTBLCOMBOBOX** <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a>Parâmetros

_n_
  
> Controle de edição de número de caracteres que podem ser inseridos na caixa de combinação. 
    
_u_
  
> Nome para a nova estrutura.
    
## <a name="remarks"></a>Comentários

A macro **SizedDtblComboBox** permite definir uma caixa de combinação quando o comprimento da cadeia de caracteres habilitados é conhecido. A nova estrutura é criada com os seguintes membros: 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

Para usar um ponteiro para a estrutura resultante de macro **SizedDtblComboBox** como um ponteiro de estrutura **DTBLCOMBOBOX** , execute a seguinte projeção: 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a>Confira também

- [DTBLCOMBOBOX](dtblcombobox.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)

