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
ms.openlocfilehash: 5b2138ff3091f70313344d5b38d8225d572d8e70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426496"
---
# <a name="trunc-function"></a>Função TRUNC

Retorna um número truncado para o número especificado de dígitos.
  
## <a name="syntax"></a>Sintaxe

TRUNCAr (* * *número* * *, * * *dígitos* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O número a ser truncado.  <br/> |
| _dígitos_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O número de dígitos para o qual truncar o _número_.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Numéricos.
  
## <a name="remarks"></a>Comentários

Se o número de _dígitos_ for maior que 0, o número será truncado para o _número_ de _dígitos_ à direita do decimal. Se o número de _dígitos_ for 0, _núm_ será truncado para um inteiro. Se o número de _dígitos_ for menor que 0, o número será truncado para o _número_ de _dígitos_ à esquerda do decimal. 
  
## <a name="example-1"></a>Exemplo 1

TRUNCAR (123.654, 2)
  
Retornará 123,65.
  
## <a name="example-2"></a>Exemplo 2

TRUNCAR (123.654, 0)
  
Retornará 123.
  
## <a name="example-3"></a>Exemplo 3

TRUNCAR (123.654,-1)
  
Retornará 120.
  

