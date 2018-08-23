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
ms.openlocfilehash: 0985ed0c5d4482bb22f46bdc9198afc343c61e5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565533"
---
# <a name="lpropcompareprop"></a>LPropCompareProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara dois valores de propriedade para determinar se eles são iguais. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a>Parâmetros

 _lpSPropValueA_
  
> [in] Ponteiro para uma estrutura [SPropValue](spropvalue.md) definindo o primeiro valor de propriedade a ser comparada. 
    
 _lpSPropValueB_
  
> [in] Ponteiro para uma estrutura **SPropValue** definindo o segundo valor da propriedade a ser comparada. 
    
## <a name="return-value"></a>Valor retornado

 **LPropCompareProp** retorna um dos seguintes valores para a maioria dos tipos de propriedade: 
  
- Menor do que zero se o valor indicado pelo parâmetro _lpSPropValueA_ é menor do que indicado pelo parâmetro _lpSPropValueB_ . 
    
- Maior do que zero se o valor indicado pelo _lpSPropValueA_ é maior do que indicado pelo _lpSPropValueB_.
    
- Zero se o valor indicado pelo _lpSPropValueA_ equivale ao valor indicado pelo _lpSPropValueB_. 
    
Para tipos de propriedade que não tenham nenhuma intrínsecas pedidos, como Boolean ou tipos de erro, a função **LPropCompareProp** retorna um valor indefinido se os dois valores de propriedade não são iguais. Esse valor indefinido é diferente de zero e consistente em chamadas. 
  
## <a name="remarks"></a>Comentários

Use a função de **LPropCompareProp** somente se os tipos de duas propriedades a serem comparadas são iguais. 
  
Antes de chamar **LPropCompareProp**, um aplicativo cliente ou um provedor de serviços deve recuperar as propriedades para comparação com uma chamada ao método [IMAPIProp::GetProps](imapiprop-getprops.md) . Quando um cliente ou provedor chamadas **LPropCompareProp**, a função examina primeiro as marcas de propriedade para certificar-se de que a comparação dos valores de propriedade é válida. A função compara os valores de propriedade, retornando um valor apropriado. 
  
Se os valores de propriedade são diferentes, **LPropCompareProp** determina qual é o maior. As propriedades que compara **LPropCompareProp** não precisará pertencem ao mesmo objeto. 
  

