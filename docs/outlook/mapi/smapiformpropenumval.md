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
ms.openlocfilehash: 2c49a17389a9bfc998f892e0becf96dca4cd773f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578714"
---
# <a name="smapiformpropenumval"></a>SMAPIFormPropEnumVal

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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

