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
ms.openlocfilehash: ccfb503f62ef039700f79cd8852883685f329dfe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766615"
---
# <a name="fpropexists"></a>FPropExists

  
  
**Aplica-se a**: Outlook 
  
Procura uma marca de propriedade fornecida em uma interface de [IMAPIProp](imapipropiunknown.md) ou um derivado do **IMAPIProp**, como [IMessage](imessageimapiprop.md) ou [IMAPIFolder](imapifolderimapicontainer.md). 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Parâmetros

 _pobj_
  
> [in] Ponteiro para a interface **IMAPIProp** ou derivados **IMAPIProp** dentro do qual procurar a marca de propriedade. 
    
 _ulPropTag_
  
> [in] Marca de propriedade a ser procurado.
    
## <a name="return-value"></a>Valor retornado

VERDADEIRO 
  
> Foi encontrada uma correspondência para a marca de propriedade fornecida. 
    
FALSO 
  
> Não foi encontrada uma correspondência para a marca de propriedade fornecida.
    
## <a name="remarks"></a>Comentários

Se a marca de propriedade no parâmetro _ulPropTag_ tiver tipo PT_UNSPECIFIED, a função **FPropExists** procura por uma correspondência com base apenas no identificador de propriedade. Caso contrário, a correspondência diferencia para a marca de propriedade inteira, incluindo o tipo. 
  

