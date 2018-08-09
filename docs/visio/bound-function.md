---
title: Função BOUND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60099
localization_priority: Normal
ms.assetid: 36374d78-1028-bd7f-6282-66555ee31306
description: Restringe o valor de uma célula a um intervalo ou série de intervalos.
ms.openlocfilehash: 2f6228828fee8fa1831bb0d3a714fca068808652
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771441"
---
# <a name="bound-function"></a>Função BOUND

Restringe o valor de uma célula a um intervalo ou série de intervalos.
  
## <a name="syntax"></a>Sintaxe

LIGADO (* * *valor* * *, * * *tipo* * *, * * *Ignorar* * *, * * *valor1* * *, * * *value2* * * * * * [, ignorar, value1(n), value2(n), …] * * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _value_ <br/> |Obrigatório  <br/> |**Numérico** <br/> |O valor que está sendo restringido no momento.  <br/> |
| _type_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |Se a restrição é inclusive (0), exclusive (1) ou desativada (2).
  <br/> |
| _Ignorar_ <br/> |Obrigatório  <br/> |**Boolean** <br/> | TRUE para ignorar o intervalo; FALSO para restringir o valor da célula ao intervalo.  <br/> |
| _value1_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |O primeiro valor de um intervalo.
  <br/> |
| _Value2_ <br/> |Obrigatório  <br/> |**Numérico** <br/> |O segundo valor de um intervalo.  <br/> |
   
## <a name="remarks"></a>Comentários

Use a função BOUND para restringir uma célula valor a um limite superior e limite inferior, por exemplo, para controlar objetos que não devem ser alongados acima ou abaixo uma altura de mínima ou máxima. A restrição é possível incluir ou excluir o intervalo ou intervalos. Se o valor atual não seja restringido, defina o parâmetro _type_ para 2 (desabilitado). 
  
Você pode definir vários intervalos fornecendo várias ocorrências dos parâmetros _Ignorar_, _value1_e _value2_ . Use o parâmetro _Ignorar_ para desativar restrições através de um determinado intervalo. 
  
A fórmula contendo a função BOUND não é substituída quando seu valor é alterado; em vez disso, ela é preservada e o novo valor é colocado no parâmetro _value_ . 
  
## <a name="example-1"></a>Exemplo 1

Este exemplo utiliza a função BOUND para forçar uma alça de controle a ficar dentro da caixa de limite de uma forma. 
  
Controls. X1 = BOUND (largura\*0,5, 0, FALSO, largura\*0, largura\*1)
  
Controls. y1 = BOUND (altura\*0,5, 0, FALSO, altura\*0, altura\*1)
  
## <a name="example-2"></a>Exemplo 2

Este exemplo utiliza a função BOUND para restringir a largura de uma forma a 2 polegadas, 4 polegadas ou 6 polegadas. 
  
Width = BOUND(, 0, FALSO, 2 pol, 2 pol, FALSO, 4 pol, 4 pol, FALSO, 6 pol, 6 pol)
  

