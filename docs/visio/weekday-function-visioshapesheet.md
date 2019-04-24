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
description: Retorna um inteiro, de 1 a 7, representando o dia da semana em DateTime ou expressão.
ms.openlocfilehash: 7c5d467d8c6ff14b99b64b8b0462d21d0b769998
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285241"
---
# <a name="weekday-function-visioshapesheet"></a>Função WEEKDAY (VisioShapeSheet)

Retorna um inteiro, de 1 a 7, representando o dia da semana em _DateTime_ ou _expressão_.
  
## <a name="syntax"></a>Sintaxe

WEEKDAY ("* * *DateTime* * *" | * * *expressão* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obrigatório  <br/> |**String** <br/> | Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.  <br/> |
| _expressão_ <br/> |Obrigatório  <br/> |**Vai** <br/> |Qualquer expressão que gere data e hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Numeric** <br/> |O identificador de local a ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Inteiro
  
## <a name="remarks"></a>Comentários

O componente de hora em _DateTime_ ou _expression_ é Descartado. 
  
O resultado corresponde a segunda-feira (1) a domingo (7). Não é feito nenhum arredondamento. Se _DateTime_ estiver faltando ou não puderem ser interpretados como uma data ou hora válida, a função retornará um #VALUE! #NUM! 
  
A função WEEKDAY também aceita um valor de número único para _expressão_ em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899. 
  
## <a name="example-1"></a>Exemplo 1

WEEKDAY("30 de maio de 1999")
  
Retornará 7.
  
## <a name="example-2"></a>Exemplo 2

WEEKDAY(DATEVALUE("30 de maio de 1999")+2 ed.)
  
Retornará 2.
  
## <a name="example-3"></a>Exemplo 3

DIA DA SEMANA (35880.6337)
  
Retornará 4.
  

