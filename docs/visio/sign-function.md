---
title: Função SIGN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251497
localization_priority: Normal
ms.assetid: fdc032c2-d0bd-1592-de3f-33c478d066ee
description: Retorna um valor que representa o sinal de um número.
ms.openlocfilehash: 5f812dc4313e15df5d66a919707e7cdbb79f94b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772993"
---
# <a name="sign-function"></a>Função SIGN

Retorna um valor que representa o sinal de um número. 
  
## <a name="syntax"></a>Sintaxe

ENTRADA (* * *número* * *, * * *fuzzing* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Numérico** <br/> | O número para o qual deseja determinar o sinal.  <br/> |
| _dados simulados_ <br/> |Opcional  <br/> |**Numérico** <br/> |Especifica o quanto o número deve estar próximo do zero para ser considerado igual a zero.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Numérico
  
## <a name="remarks"></a>Comentários

A função SIGN retornará 1 se _Núm_ for positivo, 0 se _Núm_ for zero ou -1 se _Núm_ for negativo. 
  
Specifyin um valor _indefinido_ ajuda a evitar erros de arredondamento de pontos flutuantes quando um cálculo é quase zero. Se você não especificar um valor _indefinido_ , o Visio utilizará 1E-9 (0,000000001). Convém fornecer um valor diferente, quando você dimensionar desenhos ou quando quiser uma comparação exata. 
  
## <a name="example-1"></a>Exemplo 1

SIGN(-5)
  
Retornará -1.
  
## <a name="example-2"></a>Exemplo 2

SIGN(0)
  
Retornará 0.
  
## <a name="example-3"></a>Exemplo 3

SIGN(0.00000000001)
  
Retornará 0.
  
## <a name="example-4"></a>Exemplo 4

SIGN(0.00000000001,0)
  
Retornará 1.
  

