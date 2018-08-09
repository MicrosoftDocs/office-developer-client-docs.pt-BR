---
title: Função DAYOFYEAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251416
localization_priority: Normal
ms.assetid: 154d76a2-81f5-d8b1-b665-26dbae5da615
description: Retorna um inteiro, de 1 a 366, representando o dia sequencial do ano em datetime ou expression. A função DAYOFYEAR utiliza o calendário gregoriano.
ms.openlocfilehash: 2fd80a2554c268d276deaa524a9d98eebc6a48d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771700"
---
# <a name="dayofyear-function"></a>Função DAYOFYEAR

Retorna um inteiro, de 1 a 366, representando o dia sequencial do ano em _datetime_ ou _expression_. A função DAYOFYEAR utiliza o calendário gregoriano.
  
## <a name="syntax"></a>Sintaxe

DAYOFYEAR ("* * *datetime* * *" | * * *expressão* * * [, * * *lcid* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obrigatório  <br/> |**String** <br/> |Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.  <br/> |
| _expressão_ <br/> |Obrigatório  <br/> |**String** <br/> |Qualquer expressão que gere data e hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> |Especifica o identificador de local para ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Inteiro
  
## <a name="remarks"></a>Comentários

Qualquer componente de hora em _datetime_ ou _expression_ é desconsiderado. 
  
O resultado corresponde à 1º de janeiro a 31 de dezembro. É feito nenhum arredondamento. Se _datetime_ estiver faltando ou não puder ser interpretada como uma data ou hora válida, a função retornará um erro. 
  
A função DAYOFYEAR também aceita um valor de número único para _expression_ em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899. 
  
## <a name="example-1"></a>Exemplo 1

DAYOFYEAR("30 de maio de 1997 13:45:24")
  
Retornará 150.
  
## <a name="example-2"></a>Exemplo 2

DAYOFYEAR(DATEVALUE("30 de maio de 1997")+7 ed.)
  
Retornará 157.
  
## <a name="example-3"></a>Exemplo 3

DAYOFYEAR(35580.6337)
  
Retornará 150.
  

