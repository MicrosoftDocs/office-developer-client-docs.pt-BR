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
ms.openlocfilehash: 4d060d62deb685b4691846c2b8e48a82ae3195ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770468"
---
# <a name="smapiverb"></a>SMAPIVerb

  
  
**Aplica-se a**: Outlook 
  
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

