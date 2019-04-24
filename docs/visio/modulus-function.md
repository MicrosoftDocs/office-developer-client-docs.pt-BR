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
description: Retorna o resto (módulo) que resulta quando um número é dividido por um divisor.
ms.openlocfilehash: f6b713b1b3a9d2afa85f49de9d451642a00d8dad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356991"
---
# <a name="modulus-function"></a>Função MODULUS

Retorna o resto (módulo) que resulta quando um número é dividido por um divisor.
  
## <a name="syntax"></a>Sintaxe

MÓDULO (* * *número* * *, * * *divisor* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Número** <br/> |O dividendo.  <br/> |
| _divisor_ <br/> |Obrigatório  <br/> |**Número** <br/> |O divisor.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Número
  
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
  

