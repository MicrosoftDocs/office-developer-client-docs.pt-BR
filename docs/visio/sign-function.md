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
ms.openlocfilehash: 34bbbab17de94b0a8c95b4b0bfd3829a06dc7e70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357453"
---
# <a name="sign-function"></a>Função SIGN

Retorna um valor que representa o sinal de um número. 
  
## <a name="syntax"></a>Sintaxe

ASSINAR (* * *número* * *, * * *difusão* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Numeric** <br/> | O número para o qual deseja determinar o sinal.  <br/> |
| _difusa_ <br/> |Opcional  <br/> |**Numeric** <br/> |Especifica o quanto o número deve estar próximo do zero para ser considerado igual a zero.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Numeric
  
## <a name="remarks"></a>Comentários

A função SIGN retornará 1 se _núm_ for positivo, 0 se _núm_ for zero ou-1 se _núm_ for negativo. 
  
Especificar um valor de _difusão_ ajuda a evitar erros de ponto flutuante roundoff quando um cálculo é quase zero. Se você não especificar um valor de _difusão_ , o Visio usará 1e-9 (0, 1). Convém fornecer um valor diferente ao colocar o desenho em escala ou quando desejar obter uma comparação exata. 
  
## <a name="example-1"></a>Exemplo 1

SINAL (-5)
  
Retornará -1.
  
## <a name="example-2"></a>Exemplo 2

SINAL (0)
  
Retornará 0.
  
## <a name="example-3"></a>Exemplo 3

SINAL (0.00000000001)
  
Retornará 0.
  
## <a name="example-4"></a>Exemplo 4

SINAL (0.00000000001, 0)
  
Retornará 1.
  

