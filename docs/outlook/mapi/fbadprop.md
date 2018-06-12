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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 39e10e9139036cc86ec93ea24a89b98125ea6e83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766519"
---
# <a name="fbadprop"></a>FBadProp

  
  
**Aplica-se a**: Outlook 
  
Valida uma propriedade especificada. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a>Par�metros

 _lpprop_
  
> [in] Uma estrutura de [SPropValue](spropvalue.md) definindo a propriedade a ser validado. 
    
## <a name="return-value"></a>Valor retornado

VERDADEIRO 
  
> A propriedade especificada é inválida. 
    
FALSO 
  
> A propriedade especificada é válida.
    
## <a name="remarks"></a>Coment�rios

Um provedor de serviços pode chamar a função **FBadProp** por vários motivos, por exemplo, para se preparar para uma chamada ao método [IMAPIProp::SetProps](imapiprop-setprops.md) a definição de uma propriedade. **FBadProp** valida a propriedade especificada, dependendo do tipo de propriedade. Por exemplo, se a propriedade for Boolean, **FBadProp** disponibilizar sures que seu valor é TRUE ou FALSE. Se a propriedade for binária, **FBadProp** verifica o ponteiro e o tamanho e certifica-se de que ele está alocado corretamente. 
  
## <a name="see-also"></a>Confira também



[FBadPropTag](fbadproptag.md)

