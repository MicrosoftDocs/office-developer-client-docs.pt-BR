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
ms.openlocfilehash: 353bc574ca5987d71faf4841744de30a3d6c3f19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435408"
---
# <a name="smapiformpropenumval"></a>SMAPIFormPropEnumVal

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Mapeia um valor de número inteiro enumerado para um nome de exibição para esse valor. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiform. h  <br/> |
   
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

Quando um usuário seleciona um nome de exibição de um formulário, o valor de enumeração correspondente do nome é armazenado usando a implementação da interface [IMAPIProp](imapipropiunknown.md) que está associada ao formulário. 
  
## <a name="see-also"></a>Confira também



[SMAPIFormProp](smapiformprop.md)
  
[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)

