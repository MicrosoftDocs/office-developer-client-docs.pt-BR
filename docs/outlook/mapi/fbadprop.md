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
ms.openlocfilehash: d899c8af541da231b015f6178eb7bc8f0ffd86e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426713"
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

