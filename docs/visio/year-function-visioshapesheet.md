---
title: Função YEAR (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251513
localization_priority: Normal
ms.assetid: acc136ef-9946-7c12-a467-9ded732a3549
description: Retorna um inteiro que representa o ano gregoriano em DateTime ou Expression, formatado de acordo com o estilo de data curta definido pelas configurações de região e idioma atuais do sistema.
ms.openlocfilehash: c9bacd34557d365841171bee5c9f4683e6a3d296
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351650"
---
# <a name="year-function-visioshapesheet"></a>Função YEAR (VisioShapeSheet)

Retorna um inteiro que representa o ano gregoriano em _DateTime_ ou _expression_, formatado de acordo com o estilo de data curta definido pelas configurações de região e idioma atuais do sistema.
  
## <a name="syntax"></a>Sintaxe

YEAR ("* * *DateTime* * *" | * * *expressão* * * [, * * *LCID* * *]) 
  
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
  
Não é feito nenhum arredondamento. Se _DateTime_ estiver ausente ou não puder ser interpretado como uma data ou hora válida, Year retornará um erro. 
  
A função YEAR também aceita um valor de número único para _expressão_ em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899. 
  
## <a name="example-1"></a>Exemplo 1

YEAR ("10/27/2007 13:45:24")
  
Retornará 2007.
  
## <a name="example-2"></a>Exemplo 2

YEAR(DATEVALUE("25 de dez de 2006") + 7 ed.)
  
Retornará 2007.
  
## <a name="example-3"></a>Exemplo 3

ANO (35580.6337)
  
Retornará 1997.
  

