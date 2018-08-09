---
title: FLAGLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLAGLIST
api_type:
- COM
ms.assetid: b4c0655c-1a3a-4f89-a977-0431db596512
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2cf5ff69e8453b2da26fd5044823ddf4f99a9f45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766566"
---
# <a name="flaglist"></a>FLAGLIST

  
  
**Aplica-se a**: Outlook 
  
Contém uma lista dos sinalizadores usados para indicar o status das entradas de endereço durante o processo de resolução de nome.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a>Members

 **cFlags**
  
> Contagem de sinalizadores MAPI-definidos na lista.
    
 **ulFlags**
  
> Uma matriz dos sinalizadores que fornece o status da operação de resolução de nome de um destinatário. Sinalizadores a seguir podem ser definidos:
    
MAPI_AMBIGUOUS 
  
> O destinatário foi resolvido, mas não a um identificador exclusivo de entrada. Outros contêineres do catálogo de endereços não devem tentar resolver o destinatário. 
    
MAPI_RESOLVED 
  
> O destinatário foi resolvido para um identificador exclusivo de entrada. Outros contêineres do catálogo de endereços não devem tentar resolver o destinatário. 
    
MAPI_UNRESOLVED 
  
> A entrada não foi resolvida. Outros contêineres do catálogo de endereços devem tentar resolver o destinatário.
    
## <a name="remarks"></a>Comentários

A estrutura **FLAGLIST** é usada como um parâmetro para [IABContainer:: ResolveNames](iabcontainer-resolvenames.md). Cada um dos destinatários ser resolvido está incluída em uma estrutura [ADRLIST](adrlist.md) . Como o contêiner de catálogo de endereços tenta resolver cada destinatário, ele define o sinalizador apropriado na entrada correspondente na estrutura **FLAGLIST** . Todas as entradas na estrutura de **FLAGLIST** estão na mesma ordem como as entradas na estrutura de **ADRLIST** . Isso facilita associar a um destinatário de uma configuração de sinalizador. 
  
## <a name="see-also"></a>Confira também



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[Estruturas MAPI](mapi-structures.md)

