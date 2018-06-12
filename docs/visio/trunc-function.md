---
title: Função TRUNC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251508
localization_priority: Normal
ms.assetid: 62f074ef-5bf8-df1e-d826-fc1027a36501
description: Retorna um número truncado para o número especificado de dígitos.
ms.openlocfilehash: 8f6a9798391d308a234469d93bc8f481de5fc8da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773180"
---
# <a name="trunc-function"></a>Função TRUNC

Retorna um número truncado para o número especificado de dígitos.
  
## <a name="syntax"></a>Sintaxe

TRUNC (* * *número* * *, * * *número de dígitos* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Numérico** <br/> |O número a ser truncado.  <br/> |
| _número de dígitos_ <br/> |Obrigatório  <br/> |**Numérico** <br/> |O número de dígitos para o qual truncar _number_.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Numérico.
  
## <a name="remarks"></a>Comentários

Se o _número de dígitos_ for maior do que 0, o _número_ será truncada para o _número de dígitos_ à direita da vírgula decimal. Se o _número de dígitos_ for 0, o _número_ será truncada para um número inteiro. Se o _número de dígitos_ for menor que 0, o _número_ será truncada para o _número de dígitos_ à esquerda da vírgula decimal. 
  
## <a name="example-1"></a>Exemplo 1

TRUNC(123.654,2)
  
Retornará 123,65.
  
## <a name="example-2"></a>Exemplo 2

TRUNC(123.654,0)
  
Retornará 123.
  
## <a name="example-3"></a>Exemplo 3

TRUNC(123.654,-1)
  
Retornará 120.
  

