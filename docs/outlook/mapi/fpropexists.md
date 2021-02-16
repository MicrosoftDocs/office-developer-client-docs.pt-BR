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
  
Procura uma determinada marca de propriedade em uma interface [IMAPIProp](imapipropiunknown.md) ou uma interface derivada de **IMAPIProp**, como [IMessage](imessageimapiprop.md) ou [IMAPIFolder](imapifolderimapicontainer.md). 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
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
  
> [in] Ponteiro para a interface ou interface **IMAPIProp** derivada de **IMAPIProp** na qual procurar a marca de propriedade. 
    
 _ulPropTag_
  
> [in] Marca de propriedade para a qual pesquisar.
    
## <a name="return-value"></a>Valor de retorno

TRUE 
  
> Uma match for the given property tag was found. 
    
FALSE 
  
> Uma match for the given property tag was not found.
    
## <a name="remarks"></a>Comentários

Se a marca de propriedade no  _parâmetro ulPropTag_ tiver o tipo PT_UNSPECIFIED, a **função FPropExists** procura uma combinação com base apenas no identificador de propriedade. Caso contrário, a combinação é para a marca de propriedade inteira, incluindo o tipo. 
  

