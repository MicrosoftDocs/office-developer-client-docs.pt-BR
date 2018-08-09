---
title: Função MODULUS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251465
localization_priority: Normal
ms.assetid: cb6326a5-1bf8-b6a3-5c0d-d38c071353a5
description: Retorna o resto que resulta quando um número é dividido por um divisor.
ms.openlocfilehash: 4e2ef7acf9dc04e788cb2b8a0ff737f12a79c61a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772399"
---
# <a name="modulus-function"></a>Função MODULUS

Retorna o resto que resulta quando um número é dividido por um divisor.
  
## <a name="syntax"></a>Sintaxe

MODULUS (* * *número* * *, * * *divisor* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Número** <br/> |O dividendo.  <br/> |
| _divisor_ <br/> |Obrigatório  <br/> |**Número** <br/> |O divisor.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Number
  
## <a name="remarks"></a>Comentários

O resultado tem o mesmo sinal do divisor. Um erro de #DIV/0! será retornado se o divisor for 0. 
  
Na maioria das situações, a função MODULUS deve ser usada em vez da função MOD. 
  
## <a name="example-1"></a>Exemplo 1

MODULUS(5, 1,4)
  
Retornará 0,8.
  
## <a name="example-2"></a>Exemplo 2

MODULUS(5, -1,4)
  
Retornará -0,6.
  
## <a name="example-3"></a>Exemplo 3

MODULUS(-5, 1,4)
  
Retornará 0,6.
  
## <a name="example-4"></a>Exemplo 4

MODULUS(-5, -1,4)
  
Retornará -0,8.
  

