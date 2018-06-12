---
title: Função WEEKDAY (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251512
localization_priority: Normal
ms.assetid: f2625ef8-3bdb-5a8d-48b9-149be0592533
description: Retorna um inteiro, de 1 a 7, que representa o dia da semana em datetime ou expression.
ms.openlocfilehash: decc89c93d175b357cdfe2b8377d04517b92ccab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773281"
---
# <a name="weekday-function-visioshapesheet"></a>Função WEEKDAY (VisioShapeSheet)

Retorna um inteiro, de 1 a 7, que representa o dia da semana em _datetime_ ou _expression_.
  
## <a name="syntax"></a>Sintaxe

WEEKDAY ("* * *datetime* * *" | * * *expressão* * * [, * * *lcid* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obrigatório  <br/> |**String** <br/> | Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.  <br/> |
| _expressão_ <br/> |Obrigatório  <br/> |**Varia** <br/> |Qualquer expressão que gere data e hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Numérico** <br/> |O identificador de local a ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Inteiro
  
## <a name="remarks"></a>Comentários

O componente de hora em _datetime_ ou _expression_ é desconsiderado. 
  
O resultado corresponde à segunda (1) a domingo (7). É feito nenhum arredondamento. Se _datetime_ estiver faltando ou não puder ser interpretada como uma data ou hora válida, a função retornará um #VALUE! erro. 
  
A função WEEKDAY também aceita um valor de número único para _expression_ em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899. 
  
## <a name="example-1"></a>Exemplo 1

WEEKDAY("30 de maio de 1999")
  
Retornará 7.
  
## <a name="example-2"></a>Exemplo 2

WEEKDAY(DATEVALUE("30 de maio de 1999")+2 ed.)
  
Retornará 2.
  
## <a name="example-3"></a>Exemplo 3

WEEKDAY(35880.6337)
  
Retornará 4.
  

