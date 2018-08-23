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
ms.openlocfilehash: cf84c7d94e67da0ce7453829042e7be0d4e313f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585546"
---
# <a name="flatentry"></a>FLATENTRY

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma estrutura [ENTRYID](entryid.md) mais uma contagem de bytes que especifica o tamanho da estrutura **ENTRYID** . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
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
  
> O identificador de entrada completa que inclui a matriz de sinalizadores e dados binários.
    
## <a name="remarks"></a>Comentários

Uma estrutura **FLATENTRY** é semelhante a uma estrutura [ENTRYID](entryid.md) . No entanto, há algumas diferenças: 
  
- Uma estrutura **FLATENTRY** armazena o tamanho do identificador de entrada; Não suporta **ENTRYID** . 
    
- Uma estrutura **FLATENTRY** armazena os dados de sinalizador junto com o restante do identificador de entrada; **ENTRYID** armazenando-as separadamente. 
    
- Uma estrutura **FLATENTRY** é usada para armazenar um identificador de entrada em um arquivo ou passá-la em um fluxo de bytes, enquanto uma estrutura **ENTRYID** é usada pelos métodos interface [IMAPIProp](imapipropiunknown.md) e pelos seguintes métodos **OpenEntry** : [IABLogon: : OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- Uma estrutura **FLATENTRY** é usada para armazenar um identificador de entrada em um arquivo ou passá-la em um fluxo de bytes. Uma estrutura **ENTRYID** é usada para armazenar um identificador de entrada no disco. 
    
## <a name="see-also"></a>Confira também



[ENTRYID](entryid.md)


[Estruturas MAPI](mapi-structures.md)

