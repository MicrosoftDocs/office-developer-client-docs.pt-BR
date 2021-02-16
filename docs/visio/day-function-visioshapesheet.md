---
title: Função DAY (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251415
localization_priority: Normal
ms.assetid: 3b0842ae-6893-2d7b-6cb2-8905198fae30
description: Retorna um número inteiro, de 1 a 31, representando o dia em datetime ou expression. A função DAY usa o calendário gregoriano.
ms.openlocfilehash: 49c29d5dc25bf11599f89a20cb2bc2367bd74187
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360289"
---
# <a name="day-function-visioshapesheet"></a>Função DAY (VisioShapeSheet)

Retorna um número inteiro, de 1 a 31, representando o dia em _datetime_ ou _expression_. A função DAY usa o calendário gregoriano.
  
## <a name="syntax"></a>Sintaxe

DAY(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ]) 
  
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
  
Não são feitos arredondamentos. Se _datetime_ estiver faltando ou não puder ser convertida para um resultado válido, a função retornará um erro. 
  
A função DAY também aceita um valor de número único para _expression_ em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899. 
  
## <a name="example-1"></a>Exemplo 1

DAY("30 de maio de 1997 15:45:24")
  
Retornará 30.
  
## <a name="example-2"></a>Exemplo 2

DAY(DATEVALUE("30 de maio de 1997")+7 ed.)
  
Retornará 6.
  
## <a name="example-3"></a>Exemplo 3

DAY(35580.6337)
  
Retornará 30.
  

