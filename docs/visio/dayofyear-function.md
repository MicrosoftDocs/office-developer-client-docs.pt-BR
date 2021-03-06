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
description: Retorna um inteiro, de 1 a 366, que representa o dia sequencial do ano em data e hora ou expressão. A função DAYOFYEAR usa o calendário Gregoriano.
ms.openlocfilehash: 30c0331a57282baee97e81689b6a8f362581b8f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439448"
---
# <a name="dayofyear-function"></a>Função DAYOFYEAR

Retorna um inteiro, de 1 a 366, que representa o dia sequencial do ano em   _data e hora_ ou  _expressão_. A função DAYOFYEAR usa o calendário Gregoriano.
  
## <a name="syntax"></a>Sintaxe

DAYOFYEAR(" ** *datetime* ** "| ** *expressão* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Obrigatório  <br/> |**String** <br/> |Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula contendo uma data e hora.  <br/> |
| _expression_ <br/> |Obrigatório  <br/> |**String** <br/> |Qualquer expressão que produza uma data e hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> |Especifica o identificador de local para ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Inteiro
  
## <a name="remarks"></a>Comentários

Qualquer componente de tempo em _datetime_ ou _expression_ é descartado. 
  
O resultado corresponde de 1 de janeiro a 31 de dezembro. Não é feito nenhum arredondamento. Se _datetime_ estiver ausente ou não puder ser interpretado como uma data ou hora válida, a função retornará um erro. 
  
A função DAYOFYEAR também aceita um único valor numérico para  _expressão_ em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899. 
  
## <a name="example-1"></a>Exemplo 1

DAYOFYEAR("30 de maio de 1997 13:45:24")
  
Retorna 150.
  
## <a name="example-2"></a>Exemplo 2

DAYOFYEAR(DATEVALUE("30 de maio de 1997")+7 ed.)
  
Retornará 157.
  
## <a name="example-3"></a>Exemplo 3

DAYOFYEAR (35580.6337)
  
Retornará 150.
  

