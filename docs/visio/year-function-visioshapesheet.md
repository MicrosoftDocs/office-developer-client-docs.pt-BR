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
description: Retorna um inteiro que representa o ano Gregoriano em data e hora ou expressão, formatado de acordo com o estilo de data curta definido pelas configurações atuais de Região e Idioma do sistema.
ms.openlocfilehash: c9bacd34557d365841171bee5c9f4683e6a3d296
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420707"
---
# <a name="year-function-visioshapesheet"></a>Função YEAR (VisioShapeSheet)

Retorna um inteiro que representa o ano Gregoriano em  _data e_ hora ou expressão  _,_ formatado de acordo com o estilo de data curta definido pelas configurações atuais de Região e Idioma do sistema.
  
## <a name="syntax"></a>Sintaxe

YEAR(" ** *datetime* ** "| ** *expressão* ** [, ** *lcid* ** ]) 
  
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
  
Não são feitos arredondamentos. Se  _a data e_ hora não puderem ser interpretadas como uma data ou hora válidas, YEAR retornará um erro. 
  
A função YEAR também aceita um  valor de número único para a expressão em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899. 
  
## <a name="example-1"></a>Exemplo 1

YEAR("27/10/2007 13:45:24")
  
Retornará 2007.
  
## <a name="example-2"></a>Exemplo 2

YEAR(DATEVALUE("25 de dez de 2006") + 7 ed.)
  
Retornará 2007.
  
## <a name="example-3"></a>Exemplo 3

YEAR(35580.6337)
  
Retornará 1997.
  

