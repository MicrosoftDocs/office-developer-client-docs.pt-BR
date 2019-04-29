---
title: FPropExists
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropExists
api_type:
- COM
ms.assetid: 33c00752-cdc1-4cbe-8fca-6b06c78bd362
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7190065c687524302bae362a2e25d3848e17d1bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429485"
---
# <a name="fpropexists"></a>FPropExists

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Procura uma determinada marca de propriedade em uma interface do [IMAPIProp](imapipropiunknown.md) ou uma interface derivada de **IMAPIProp**, como [IMessage](imessageimapiprop.md) ou [IMAPIFolder](imapifolderimapicontainer.md). 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Parâmetros

 _pobj_
  
> no Ponteiro para a interface **IMAPIProp** ou a interface derivada de **IMAPIProp** dentro da qual procurar a marca da propriedade. 
    
 _ulPropTag_
  
> no Marca de propriedade para a qual Pesquisar.
    
## <a name="return-value"></a>Valor de retorno

TRUE 
  
> Uma correspondência para a marca de propriedade fornecida foi encontrada. 
    
FALSE 
  
> Uma correspondência para a marca de propriedade fornecida não foi encontrada.
    
## <a name="remarks"></a>Comentários

Se a marca de propriedade no parâmetro _ulPropTag_ tiver o tipo PT_UNSPECIFIED, a função **FPropExists** procurará uma correspondência com base apenas no identificador de propriedade. Caso contrário, a correspondência é para a marca de propriedade inteira, incluindo o tipo. 
  

