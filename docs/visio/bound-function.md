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
ms.openlocfilehash: 85fbe66d4e458ac4e42c9eb3c65b9a3a1d8211df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425957"
---
# <a name="bound-function"></a>Função BOUND

Restringe o valor de uma célula a um intervalo ou série de intervalos.
  
## <a name="syntax"></a>Sintaxe

BOUND (* * *Value* * *, * * *Type* * *, * * *ignore* * *, * * *value1* * *, * * *value2* * * * * * [, ignorar (n), value1 (n), value2 (n),...] * * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _value_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O valor que está sendo restringido no momento.  <br/> |
| _type_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |Se a restrição é inclusive (0), exclusive (1) ou desativada (2).  <br/> |
| _ignora_ <br/> |Obrigatório  <br/> |**Boolean** <br/> | TRUE para ignorar o intervalo; FALSE para restringir o valor da célula ao intervalo.  <br/> |
| _valor1_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O primeiro valor de um intervalo.  <br/> |
| _value2_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O segundo valor de um intervalo.  <br/> |
   
## <a name="remarks"></a>Comentários

Use a função BOUND para restringir o valor de uma célula a um limite superior ou inferior; por exemplo, para controlar objetos que não devem ser estendidos acima ou abaixo de uma altura mínima ou máxima. A restrição pode incluir ou excluir o intervalo ou intervalos. Se o valor atual não deve ser restrito, defina o parâmetro _Type_ como 2 (Disabled). 
  
Você pode definir vários intervalos fornecendo várias ocorrências dos parâmetros _ignore_, _value1_e _value2_ . Use o parâmetro _ignore_ para desabilitar as restrições por um intervalo específico. 
  
A fórmula contendo a função BOUND não é substituída quando seu valor é alterado; em vez disso, a fórmula é preservada e o novo valor é colocado no parâmetro _Value_ . 
  
## <a name="example-1"></a>Exemplo 1

Este exemplo utiliza a função BOUND para forçar uma alça de controle a ficar dentro da caixa de limite de uma forma. 
  
Controls. X1 = BOUND (largura\*0,5, 0, falso, largura\*0, largura\*1)
  
Controls. Y1 = BOUND (altura\*0,5, 0, falso, altura\*0, altura\*1)
  
## <a name="example-2"></a>Exemplo 2

Este exemplo utiliza a função BOUND para restringir a largura de uma forma a 2 polegadas, 4 polegadas ou 6 polegadas. 
  
Width = BOUND(, 0, FALSO, 2 pol, 2 pol, FALSO, 4 pol, 4 pol, FALSO, 6 pol, 6 pol)
  

