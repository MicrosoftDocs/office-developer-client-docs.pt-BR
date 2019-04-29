---
title: FLATENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRY
api_type:
- COM
ms.assetid: 03e53e08-9113-4101-84c9-ccf6d43127f6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e47f4e0d1ab9ab3ecfd53932b8ef26440134c603
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407239"
---
# <a name="flatentry"></a>FLATENTRY

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma [](entryid.md) estrutura ENTRYID mais uma contagem de bytes que especifica o tamanho da **** estrutura ENTRYID. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Macros relacionadas:  <br/> |[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a>Members

 **cb**
  
> Contagem de bytes no membro **abEntry** . 
    
 **abEntry**
  
> O identificador de entrada completo que inclui a matriz de sinalizadores e dados binários.
    
## <a name="remarks"></a>Comentários

Uma estrutura **FLATENTRY** lembra de uma estrutura [EntryID](entryid.md) . No enTanto, há algumas diferenças: 
  
- Uma estrutura **FLATENTRY** armazena o tamanho do identificador de entrada; **EntryID** não. 
    
- Uma estrutura **FLATENTRY** armazena os dados de sinalizador junto com o resto do identificador de entrada; **EntryID** as armazena separadamente. 
    
- Uma estrutura **FLATENTRY** é usada para armazenar um identificador de entrada em um arquivo ou passá-lo em um fluxo de bytes, enquanto uma estrutura **EntryID** é usada pelos métodos da interface [IMAPIProp](imapipropiunknown.md) e pelos seguintes métodos de **OpenEntry** : [IABLogon: : OpenEntry](iablogon-openentry.md), [IAddrBook:: OpenEntry](iaddrbook-openentry.md), [IMAPIContainer:](imapicontainer-openentry.md): OpenEntry, [IMAPISession:](imapisession-openentry.md): OpenEntry, [](imapisupport-openentry.md)IMAPISupport [:](imsgstore-openentry.md)OpenEntry, IMsgStore:: OpenEntry [](imslogon-openentry.md)
    
- Uma estrutura **FLATENTRY** é usada para armazenar um identificador de entrada em um arquivo ou passá-lo em um fluxo de bytes. Uma **** estrutura ENTRYID é usada para armazenar um identificador de entrada no disco. 
    
## <a name="see-also"></a>Confira também



[ENTRYID](entryid.md)


[Estruturas MAPI](mapi-structures.md)

