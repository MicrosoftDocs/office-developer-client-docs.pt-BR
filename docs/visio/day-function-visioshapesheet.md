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
ms.openlocfilehash: 07607b809aec9f50ae8981476313fc5e8dbc3423
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771690"
---
# <a name="day-function-visioshapesheet"></a>Função DAY (VisioShapeSheet)

Retorna um número inteiro, de 1 a 31, representando o dia em _datetime_ ou _expression_. A função DAY usa o calendário gregoriano.
  
## <a name="syntax"></a>Sintaxe

DIA ("* * *datetime* * *" | * * *expressão* * * [, * * *lcid* * *]) 
  
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
  
É feito nenhum arredondamento. Se _datetime_ estiver faltando ou não puder ser convertida para um resultado válido, a função retornará um erro. 
  
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
  

