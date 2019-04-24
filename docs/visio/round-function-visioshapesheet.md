---
title: Função ROUND (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
localization_priority: Normal
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Arredonda um número para a precisão representada pelo número de dígitos.
ms.openlocfilehash: 6795cbc4d99e293da06c0ec369d2cefb84f9f5b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315572"
---
# <a name="round-function-visioshapesheet"></a>Função ROUND (VisioShapeSheet)

Arredonda um número para a precisão representada pelo número de *dígitos* . 
  
## <a name="syntax"></a>Sintaxe

ARREd (* * Number * *, * * *número* de *dígitos* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Número** <br/> |O número a ser arredondado.  <br/> |
| _dígitos_ <br/> |Obrigatório  <br/> |**Número** <br/> |O número de casas decimais de precisão.  <br/> |
   
## <a name="remarks"></a>Comentários

Se o número de _dígitos_ for maior que 0, núm será arredondado para o _número_ de _dígitos_ à direita do decimal. Se o número de _dígitos_ for 0, _núm_ será arredondado para um inteiro. Se o número de _dígitos_ for menor que 0, núm será arredondado para o _número_ de _dígitos_ à esquerda do decimal. 
  
## <a name="example-1"></a>Exemplo 1

ARRED (123.654, 2)
  
Retornará 123,65.
  
## <a name="example-2"></a>Exemplo 2

ARRED (123.654, 0)
  
Retornará 124.
  
## <a name="example-3"></a>Exemplo 3

ARRED (123.654,-1)
  
Retornará 120.
  

