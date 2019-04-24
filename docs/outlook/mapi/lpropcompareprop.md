---
title: LPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPropCompareProp
api_type:
- COM
ms.assetid: f14ad568-fe45-4875-957d-415d39dc6f28
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7417ddeb814cafb954d5ab80a6dae771fd0f7a79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357432"
---
# <a name="lpropcompareprop"></a>LPropCompareProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara dois valores de propriedade para determinar se eles são iguais. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a>Parâmetros

 _lpSPropValueA_
  
> no Ponteiro para uma estrutura [SPropValue](spropvalue.md) que define o valor da primeira propriedade a ser comparada. 
    
 _lpSPropValueB_
  
> no Ponteiro para uma estrutura **SPropValue** que define o segundo valor de propriedade a ser comparado. 
    
## <a name="return-value"></a>Valor de retorno

 **LPropCompareProp** retorna um dos seguintes valores para a maioria dos tipos de propriedade: 
  
- Menor que zero se o valor indicado pelo parâmetro _lpSPropValueA_ for menor que o indicado pelo parâmetro _lpSPropValueB_ . 
    
- Maior que zero se o valor indicado por _lpSPropValueA_ for maior que o indicado por _lpSPropValueB_.
    
- Zero se o valor indicado por _lpSPropValueA_ igual ao valor indicado por _lpSPropValueB_. 
    
Para tipos de propriedade que não têm ordenação intrínseca, como tipos Boolean ou de erro, a função **LPropCompareProp** retornará um valor indefinido se os dois valores de propriedade não forem iguais. Esse valor indefinido é diferente de zero e consiste em chamadas. 
  
## <a name="remarks"></a>Comentários

Use a função **LPropCompareProp** somente se os tipos das duas propriedades a serem comparadas forem os mesmos. 
  
Antes de chamar **LPropCompareProp**, um aplicativo cliente ou provedor de serviços deve recuperar primeiro as propriedades para comparação com uma chamada para o método [IMAPIProp::](imapiprop-getprops.md) GetProps. Quando um cliente ou provedor chama **LPropCompareProp**, a função primeiro examina as marcas de propriedade para garantir que a comparação dos valores de propriedade é válida. A função, em seguida, compara os valores de propriedade, retornando um valor apropriado. 
  
Se os valores da propriedade forem diferentes, **LPropCompareProp** determinará qual deles é maior. As propriedades que o **LPropCompareProp** compara não precisam pertencer ao mesmo objeto. 
  

