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
description: Retorna um inteiro, de 1 a 7, representando o dia da semana em data e hora ou expressão.
ms.openlocfilehash: 7c5d467d8c6ff14b99b64b8b0462d21d0b769998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404803"
---
# <a name="weekday-function-visioshapesheet"></a>Função WEEKDAY (VisioShapeSheet)

Retorna um inteiro, de 1 a 7, representando o dia da semana em _data e hora_ ou _expressão._
  
## <a name="syntax"></a>Sintaxe

WEEKDAY(" ** *datetime* ** "| ** *expressão* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Obrigatório  <br/> |**String** <br/> | Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula contendo uma data e hora.  <br/> |
| _expression_ <br/> |Obrigatório  <br/> |**Varia** <br/> |Qualquer expressão que produza uma data e hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Numérica** <br/> |O identificador de local a ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Inteiro
  
## <a name="remarks"></a>Comentários

O componente de hora na  _data e_ na  _expressão_ é descartado. 
  
O resultado corresponde de segunda (1) a domingo (7). Não são feitos arredondamentos. Se  _a data e_ a hora não puderem ser interpretadas como uma data ou hora válidas, a função retornará uma #VALUE! . 
  
A função WEEKDAY também aceita um  valor de número único para a expressão em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899. 
  
## <a name="example-1"></a>Exemplo 1

WEEKDAY("30 de maio de 1999")
  
Retornará 7.
  
## <a name="example-2"></a>Exemplo 2

WEEKDAY(DATEVALUE("30 de maio de 1999")+2 ed.)
  
Retornará 2.
  
## <a name="example-3"></a>Exemplo 3

WEEKDAY(35880.6337)
  
Retornará 4.
  

