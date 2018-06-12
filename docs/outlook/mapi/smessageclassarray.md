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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 01563e3655d42abc62ea88a12f2878e5d81129d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770467"
---
# <a name="smessageclassarray"></a>SMessageClassArray

  
  
**Aplica-se a**: Outlook 
  
Contém uma matriz de ponteiros para cadeias de caracteres de classe de mensagem.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MAPIForm.h  <br/> |
|Macro relacionada:  <br/> |[CbMessageClassArray](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a>Membros

 **cValues**
  
> Contagem de ponteiros de cadeia de caracteres de classe de mensagem na matriz.
    
 **aMessageClass**
  
> Matriz de ponteiros para cadeias de caracteres de classe de mensagem.
    
## <a name="remarks"></a>Coment�rios

A estrutura **SMessageClassArray** é passada como um parâmetro nos seguintes métodos: 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>Confira também



[Estruturas MAPI](mapi-structures.md)

