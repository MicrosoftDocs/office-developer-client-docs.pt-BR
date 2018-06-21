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
ms.openlocfilehash: 2457bdf6b46a2bb44b203497f02cc9b2ff034847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/21/2018
ms.locfileid: "19772752"
---
# <a name="round-function-visioshapesheet"></a>Função ROUND (VisioShapeSheet)

Arredonda um número para a precisão representada pelo *número de dígitos* . 
  
## <a name="syntax"></a>Sintaxe

Arredondar (* * *número* * *, * * *número de dígitos* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Número** <br/> |O número a ser arredondado.  <br/> |
| _número de dígitos_ <br/> |Obrigatório  <br/> |**Número** <br/> |O número de casas decimais de precisão.  <br/> |
   
## <a name="remarks"></a>Comentários

Se o _número de dígitos_ for maior do que 0, o _número_ será arredondado pelo _número de dígitos_ à direita da vírgula decimal. Se o _número de dígitos_ for 0, o _número_ será arredondado para um número inteiro. Se o _número de dígitos_ for menor que 0, o _número_ será arredondado pelo _número de dígitos_ à esquerda da vírgula decimal. 
  
## <a name="example-1"></a>Exemplo 1

ROUND(123.654,2)
  
Retornará 123,65.
  
## <a name="example-2"></a>Exemplo 2

ROUND(123.654,0)
  
Retornará 124.
  
## <a name="example-3"></a>Exemplo 3

ROUND(123.654,-1)
  
Retornará 120.
  

