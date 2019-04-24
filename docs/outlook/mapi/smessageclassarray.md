---
title: SMessageClassArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMessageClassArray
api_type:
- COM
ms.assetid: 05f8c191-db2b-4174-8b3c-a9fdabfe6ac8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 01b42c04244d35d72dd856222b4bab543b84db45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339659"
---
# <a name="smessageclassarray"></a>SMessageClassArray

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma matriz de ponteiros para cadeias de caracteres de classe de mensagem.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiform. h  <br/> |
|Macro relacionada:  <br/> |[CbMessageClassArray](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a>Members

 **cValues**
  
> Contagem de ponteiros de cadeia de caracteres de classe de mensagem na matriz.
    
 **aMessageClass**
  
> Matriz de ponteiros para cadeias de caracteres de classe de mensagem.
    
## <a name="remarks"></a>Comentários

A estrutura **SMessageClassArray** é passada como um parâmetro nos seguintes métodos: 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>Confira também



[Estruturas MAPI](mapi-structures.md)

