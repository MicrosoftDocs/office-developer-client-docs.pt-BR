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
ms.openlocfilehash: a5e508f5f7e6554a115517da87a8eac39f39aecf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412972"
---
# <a name="flaglist"></a>FLAGLIST

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma lista de sinalizadores usados para indicar o status das entradas de endereço durante o processo de resolução de nomes.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a>Members

 **cFlags**
  
> Contagem de sinalizadores definidos por MAPI na lista.
    
 **ulFlags**
  
> Uma matriz de sinalizadores que fornece o status da operação de resolução de nome de um destinatário. Os seguintes sinalizadores podem ser definidos:
    
MAPI_AMBIGUOUS 
  
> O destinatário foi resolvido, mas não a um identificador de entrada exclusivo. Outros contêineres do catálogo de endereços não devem tentar resolver esse destinatário. 
    
MAPI_RESOLVED 
  
> O destinatário foi resolvido para um identificador de entrada exclusivo. Outros contêineres do catálogo de endereços não devem tentar resolver esse destinatário. 
    
MAPI_UNRESOLVED 
  
> A entrada não foi resolvida. Outros contêineres do catálogo de endereços devem tentar resolver esse destinatário.
    
## <a name="remarks"></a>Comentários

A estrutura da **marca de sinalizador** é usada como um parâmetro para [IABContainer:: ResolveNames](iabcontainer-resolvenames.md). Cada um dos destinatários a serem resolvidos está incluído em uma estrutura [das ADRLIST](adrlist.md) . Como o contêiner de catálogo de endereços tenta resolver cada destinatário, ele define o sinalizador apropriado na entrada correspondente na estrutura **flaglist** . Todas as entradas na estrutura **flaglist** estão na mesma ordem das entradas na estrutura **das ADRLIST** . Isso facilita a associação de uma configuração de sinalizador a um destinatário. 
  
## <a name="see-also"></a>Confira também



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[Estruturas MAPI](mapi-structures.md)

