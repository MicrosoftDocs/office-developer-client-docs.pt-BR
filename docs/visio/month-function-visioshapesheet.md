---
title: Função MONTH (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251467
localization_priority: Normal
ms.assetid: e099dbb3-c591-d934-5cfd-7728b10bd8dc
description: Retorna um inteiro de 1 a 12 que representa um mês.
ms.openlocfilehash: 71ecc7992839c871780e9b703377db37279246e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431971"
---
# <a name="month-function-visioshapesheet"></a>Função MONTH (VisioShapeSheet)

Retorna um inteiro de 1 a 12 que representa um mês.
  
## <a name="syntax"></a>Sintaxe

MONTH ("* * *DateTime* * *" | * * *expressão* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> |Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula contendo uma data e hora.  <br/> |
| _expressão_ <br/> |Obrigatório  <br/> |**String** <br/> | Qualquer expressão que produza uma data e hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> |O identificador de local a ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Inteiro
  
## <a name="remarks"></a>Comentários

O componente de hora de _DateTime_ ou _expression_ é Descartado. 
  
Não é feito nenhum arredondamento. Se a cadeia de caracteres estiver faltando ou não puder ser convertida em um resultado válido, a função MONTH retornará um erro.
  
O valor retornado é formatado de acordo com o estilo de data curta definido pelas Configurações regionais atuais do sistema.
  
A função MONTH também aceita um valor de número único para _expressão_ em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899. 
  
## <a name="example-1"></a>Exemplo 1

MONTH("30 de maio de 1999 13:45:24")
  
Retornará 5.
  
## <a name="example-2"></a>Exemplo 2

MONTH(DATEVALUE("30 de maio de 1999")+7 ed.)
  
Retornará 6.
  
## <a name="example-3"></a>Exemplo 3

MÊS (35580.6337)
  
Retornará 5.
  

