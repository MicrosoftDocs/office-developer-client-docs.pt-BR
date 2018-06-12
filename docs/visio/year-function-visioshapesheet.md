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
description: Retorna um inteiro que representa o ano gregoriano em datetime ou expression, formatado de acordo com o estilo de data curta definido pelas configurações atuais de região e idioma do sistema.
ms.openlocfilehash: aaa183730440857d8d283912f4afeb3117ef737f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773338"
---
# <a name="year-function-visioshapesheet"></a>Função YEAR (VisioShapeSheet)

Retorna um inteiro que representa o ano gregoriano em _datetime_ ou _expressão_, formatado de acordo com o estilo de data curta definido pelas configurações atuais de região e idioma do sistema.
  
## <a name="syntax"></a>Sintaxe

ANO ("* * *datetime* * *" | * * *expressão* * * [, * * *lcid* * *]) 
  
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
  
É feito nenhum arredondamento. Se _datetime_ estiver faltando ou não puder ser interpretada como uma data ou hora válida, ano retornará um erro. 
  
A função YEAR também aceita um valor de número único para _expression_ em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899. 
  
## <a name="example-1"></a>Exemplo 1

YEAR("27/10/2007 13:45:24")
  
Retornará 2007.
  
## <a name="example-2"></a>Exemplo 2

YEAR(DATEVALUE("25 de dez de 2006") + 7 ed.)
  
Retornará 2007.
  
## <a name="example-3"></a>Exemplo 3

YEAR(35580.6337)
  
Retornará 1997.
  

