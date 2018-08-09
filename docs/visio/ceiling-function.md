---
title: Função CEILING
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251405
localization_priority: Normal
ms.assetid: 1a8d6d48-7ae3-5483-28d2-5b1706088a53
description: Arredonda um número de 0 (zero) para a próxima instância do múltiplo. Se multiple não for especificado, o número será arredondado para longe de 0 do próximo número inteiro.
ms.openlocfilehash: fa982b44ea4a73e7da614c49a52cd50efd612f20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771447"
---
# <a name="ceiling-function"></a>Função CEILING

Arredonda um número de 0 (zero) para a próxima instância do _vários_. Se _vários_ não for especificado, o número será arredondado para longe de 0 do próximo número inteiro. 
  
## <a name="syntax"></a>Sintaxe

CEILING (* * *número* * *, * * *vários* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Número** <br/> |O número a ser arredondado.  <br/> |
| _vários_ <br/> |Obrigatório  <br/> |**Número** <br/> |O múltiplo para arredondar para.  <br/> |
   
## <a name="remarks"></a>Comentários

 _Número_ e _vários_ devem ter o mesmo sinal ou um #NUM! erro será retornado. Se o _número_ ou o _múltiplo_ não puder ser convertida para um valor, um #VALUE! erro será retornado. Se o _número_ ou o _múltiplo_ for 0, o resultado é 0. 
  
## <a name="example-1"></a>Exemplo 1

CEILING(3.7)
  
Retornará 4
  
## <a name="example-2"></a>Exemplo 2

CEILING(-3.7)
  
Retornará -4
  
## <a name="example-3"></a>Exemplo 3

CEILING (3,7, 0,25)
  
Retornará 3,75
  

