---
title: SMAPIFormPropEnumVal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropEnumVal
api_type:
- COM
ms.assetid: 694d40e9-cff2-435e-ad90-446044c306d2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bae750e7e940bc1417b3d225c9c81129e9da77b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770446"
---
# <a name="smapiformpropenumval"></a>SMAPIFormPropEnumVal

  
  
**Aplica-se a**: Outlook 
  
Mapeia um valor inteiro enumeradas para um nome de exibição para o valor. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MAPIForm.h  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a>Members

 **pszDisplayName**
  
> Cadeia de caracteres que contém o nome de exibição para o valor especificado no membro **nVal** . 
    
 **nVal**
  
> Um valor de enumeração para o nome de exibição apontado pelo membro **pszDisplayName** . 
    
## <a name="remarks"></a>Comentários

Quando o usuário seleciona um nome de exibição a partir de um formulário, o valor de enumeração correspondente do nome é armazenado usando a implementação de interface de [IMAPIProp](imapipropiunknown.md) que está associada ao formulário. 
  
## <a name="see-also"></a>Confira também



[SMAPIFormProp](smapiformprop.md)
  
[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)

