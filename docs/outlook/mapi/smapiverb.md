---
title: SMAPIVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerb
api_type:
- COM
ms.assetid: 45066528-2447-4178-aaa3-7513ed0b3ba4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 11f11ae2d90a951a119895f3e0e3e3ca0dbc0fc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573695"
---
# <a name="smapiverb"></a>SMAPIVerb

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve um verbo MAPI.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MAPIForm.h  <br/> |
   
```cpp
typedef struct
{
  ULONG lVerb;
  LPSTR szVerbname;
  DWORD fuFlags;
  DWORD grfAttribs;
  ULONG ulFlags; /* Either 0 or MAPI_UNICODE */
} SMAPIVerb, FAR * LPMAPIVERB;

```

## <a name="members"></a>Members

 **lVerb**
  
> Código que representa o verbo que é passado para [IMAPIForm::DoVerb](imapiform-doverb.md). Verbos padrão são definidos no arquivo de cabeçalho Exchform.h.
    
 **szVerbname**
  
> Nome para exibição do verbo como ele aparece no menu formulário.
    
 **fuFlags**
  
> Sinalizadores para o verbo.
    
 **grfAttribs**
  
> Atributos do verbo. 
    
 **ulFlags**
  
> Sinalizador que indica o formato de nome para exibição da verbo. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> O nome de exibição está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o nome de exibição é no formato ANSI.
    
## <a name="remarks"></a>Comentários

A estrutura **SMAPIVerb** é passada como um parâmetro nos seguintes métodos: 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>Confira também



[CbMessageClassArray](cbmessageclassarray.md)


[Estruturas MAPI](mapi-structures.md)

