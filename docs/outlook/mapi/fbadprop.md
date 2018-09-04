---
title: FBadProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadProp
api_type:
- HeaderDef
ms.assetid: 929330c8-e6f2-4adf-a36e-fba18fa055d4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2fbff399e088edaf3ad864f0ec7fecda3af6bc8e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578847"
---
# <a name="fbadprop"></a>FBadProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Valida uma propriedade especificada. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a>Parâmetros

 _lpprop_
  
> [in] Uma estrutura [SPropValue](spropvalue.md) que define a propriedade a ser validada. 
    
## <a name="return-value"></a>Valor de retorno

TRUE 
  
> A propriedade especificada é inválida. 
    
FALSE 
  
> A propriedade especificada é válida.
    
## <a name="remarks"></a>Comentários

Um provedor de serviços pode chamar a função **FBadProp** por diversos motivos; por exemplo, para se preparar para uma chamada para o método [IMAPIProp::SetProps](imapiprop-setprops.md) configurando uma propriedade. **FBadProp** valida a propriedade especificada, dependendo do tipo de propriedade. Por exemplo, se a propriedade é booliana, **FBadProp** garante que o respectivo valor seja TRUE ou FALSE. Quado a propriedade é binária, **FBadProp** verifica o ponteiro e o tamanho e garante que ela seja alocada corretamente. 
  
## <a name="see-also"></a>Confira também



[FBadPropTag](fbadproptag.md)

