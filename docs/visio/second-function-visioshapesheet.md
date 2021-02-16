---
title: Função SECOND (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251495
localization_priority: Normal
ms.assetid: 22005976-37c0-d2be-8e34-8aee8458e4be
description: Retorna um inteiro, de 0 a 59, que representa o componente de segundos de data e hora ou expressão.
ms.openlocfilehash: c23bbded12a3886fe3bd4dd2a3c3ba1bd6d11619
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404873"
---
# <a name="second-function-visioshapesheet"></a>Função SECOND (VisioShapeSheet)

Retorna um inteiro, de 0 a 59, que representa o componente de segundos de _data e hora_ ou _expressão._
  
## <a name="syntax"></a>Sintaxe

SECOND(" ** *datetime* ** "| ** *expressão* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Obrigatório  <br/> |**String** <br/> |Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula contendo uma data e hora.  <br/> |
| _expression_ <br/> |Obrigatório  <br/> |**String** <br/> | Qualquer expressão que produza uma data e hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Numérica** <br/> |O identificador de localidade a ser usado na avaliação de uma data e _hora não locais._ O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Inteiro
  
## <a name="remarks"></a>Comentários

O componente de data em  _data e_ hora  _ou expressão_ é descartado. 
  
Não são feitos arredondamentos. Se  _a data e_ a hora não puderem ser convertidas em um resultado válido, essa função retornará um erro. 
  
A função SECOND também aceita um  valor de número único para a expressão em que a parte decimal do resultado representa a fração de um dia desde a meia-noite. 
  
## <a name="example-1"></a>Exemplo 1

SECOND("30/05/1997 13:45:32")
  
Retornará 32.
  
## <a name="example-2"></a>Exemplo 2

SECOND(TIMEVALUE("30 de maio de 1996 12:07:45") + 7 es.)
  
Retornará 52.
  
## <a name="example-3"></a>Exemplo 3

SECOND(0,6337)
  
Retornará 32.
  

