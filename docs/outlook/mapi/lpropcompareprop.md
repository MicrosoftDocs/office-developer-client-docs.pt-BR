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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414610"
---
# <a name="lpropcompareprop"></a>LPropCompareProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara dois valores de propriedade para determinar se eles são iguais. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
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
  
> [in] Ponteiro para uma [estrutura SPropValue](spropvalue.md) definindo o primeiro valor de propriedade a ser comparado. 
    
 _lpSPropValueB_
  
> [in] Ponteiro para uma **estrutura SPropValue** definindo o segundo valor de propriedade a ser comparado. 
    
## <a name="return-value"></a>Valor de retorno

 **LPropCompareProp** retorna um dos seguintes valores para a maioria dos tipos de propriedade: 
  
- Menor que zero se o valor indicado pelo parâmetro _lpSPropValueA_ for menor que o indicado pelo parâmetro _lpSPropValueB._ 
    
- Maior que zero se o valor indicado por  _lpSPropValueA_ for maior do que o indicado por  _lpSPropValueB_.
    
- Zero se o valor indicado por  _lpSPropValueA_ for igual ao valor indicado por  _lpSPropValueB_. 
    
Para tipos de propriedade que não tenham ordenação intrínseca, como booleano ou tipos de erro, a função **LPropCompareProp** retornará um valor indefinido se os dois valores de propriedade não são iguais. Esse valor indefinido não é zero e é consistente entre chamadas. 
  
## <a name="remarks"></a>Comentários

Use a **função LPropCompareProp** somente se os tipos das duas propriedades a serem comparadas são os mesmos. 
  
Antes de **chamar LPropCompareProp**, um aplicativo cliente ou provedor de serviços deve primeiro recuperar as propriedades para comparação com uma chamada para o método [IMAPIProp::GetProps.](imapiprop-getprops.md) Quando um cliente ou provedor chama **LPropCompareProp**, a função primeiro examina as marcas de propriedade para garantir que a comparação de valores de propriedade é válida. Em seguida, a função compara os valores da propriedade, retornando um valor apropriado. 
  
Se os valores da propriedade são desapropriedade, **LPropCompareProp** determina qual deles é o maior. As propriedades comparadas **por LPropCompareProp** não devem pertencer ao mesmo objeto. 
  

