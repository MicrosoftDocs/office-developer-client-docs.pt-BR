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
description: Retorna um inteiro, de 0 a 59, que representa o componente de segundos de datetime ou expression.
ms.openlocfilehash: 5f0a3e87763bd4ea5436afe221e12477e9186356
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772846"
---
# <a name="second-function-visioshapesheet"></a>Função SECOND (VisioShapeSheet)

Retorna um inteiro, de 0 a 59, que representa o componente de segundos de _datetime_ ou _expression_.
  
## <a name="syntax"></a>Sintaxe

SEGUNDO ("* * *datetime* * *" | * * *expressão* * * [, * * *lcid* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obrigatório  <br/> |**String** <br/> |Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.  <br/> |
| _expressão_ <br/> |Obrigatório  <br/> |**String** <br/> | Qualquer expressão que gere data e hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Numeric** <br/> |O identificador de localidade a ser usado ao avaliar um não- _datetime_. O identificador de localidade é um número descrito nos arquivos de cabeçalho do sistema.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Inteiro
  
## <a name="remarks"></a>Comentários

O componente de data em _datetime_ ou _expression_ é desconsiderado. 
  
É feito nenhum arredondamento. Se _datetime_ estiver faltando ou não puder ser convertida para um resultado válido, essa função retornará um erro. 
  
A função SECOND também aceita um valor de número único para _expression_ em que a parte decimal do resultado representa a fração de um dia desde a meia-noite. 
  
## <a name="example-1"></a>Exemplo 1

DATEVALUE("30/05/97 13:45:32")
  
Retornará 32.
  
## <a name="example-2"></a>Exemplo 2

SECOND(TIMEVALUE("30 de maio de 1996 12:07:45") + 7 es.)
  
Retornará 52.
  
## <a name="example-3"></a>Exemplo 3

SECOND(0.6337)
  
Retornará 32.
  

