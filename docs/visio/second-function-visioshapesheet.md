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
description: Retorna um inteiro, 0 a 59, que representa o componente de segundos de DateTime ou expressão.
ms.openlocfilehash: c23bbded12a3886fe3bd4dd2a3c3ba1bd6d11619
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332785"
---
# <a name="second-function-visioshapesheet"></a>Função SECOND (VisioShapeSheet)

Retorna um inteiro, 0 a 59, que representa o componente de segundos de _DateTime_ ou _expressão_.
  
## <a name="syntax"></a>Sintaxe

SEGUNDO ("* * *DateTime* * *" | * * *expressão* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obrigatório  <br/> |**String** <br/> |Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.  <br/> |
| _expressão_ <br/> |Obrigatório  <br/> |**String** <br/> | Qualquer expressão que gere data e hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Numeric** <br/> |O identificador de localidade a ser usado na avaliação de um _DateTime_não local. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Inteiro
  
## <a name="remarks"></a>Comentários

O componente de data em _DateTime_ ou _expression_ é Descartado. 
  
Não é feito nenhum arredondamento. Se a _data/hora_ estiver ausente ou não puder ser convertida em um resultado válido, essa função retornará um erro. 
  
A segunda função também aceita um valor de número único para _expressão_ em que a parte decimal do resultado representa a fração de um dia desde a meia-noite. 
  
## <a name="example-1"></a>Exemplo 1

SEGUNDO ("05/30/1997 13:45:32")
  
Retornará 32.
  
## <a name="example-2"></a>Exemplo 2

SECOND(TIMEVALUE("30 de maio de 1996 12:07:45") + 7 es.)
  
Retornará 52.
  
## <a name="example-3"></a>Exemplo 3

SEGUNDO (0.6337)
  
Retornará 32.
  

