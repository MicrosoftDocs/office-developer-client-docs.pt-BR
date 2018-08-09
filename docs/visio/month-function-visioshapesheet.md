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
ms.openlocfilehash: e17803a153b4aadec34aa751da7efa077963bba5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772400"
---
# <a name="month-function-visioshapesheet"></a>Função MONTH (VisioShapeSheet)

Retorna um inteiro de 1 a 12 que representa um mês.
  
## <a name="syntax"></a>Sintaxe

MONTH ("* * *datetime* * *" | * * *expressão* * * [, * * *lcid* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obrigatório  <br/> |**String** <br/> |Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.  <br/> |
| _expressão_ <br/> |Obrigatório  <br/> |**String** <br/> | Qualquer expressão que gere data e hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> |O identificador de local a ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Inteiro
  
## <a name="remarks"></a>Comentários

O componente de hora de _datetime_ ou _expression_ é desconsiderado. 
  
Não é feito nenhum arredondamento. Se a cadeia de caracteres estiver faltando ou não puder ser convertida em um resultado válido, a função MONTH retornará um erro.
  
O valor retornado é formatado de acordo com o estilo de data curta definido pelas Configurações regionais atuais do sistema.
  
A função MONTH também aceita um valor de número único para _expression_ em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899. 
  
## <a name="example-1"></a>Exemplo 1

MONTH("30 de maio de 1999 13:45:24")
  
Retornará 5.
  
## <a name="example-2"></a>Exemplo 2

MONTH(DATEVALUE("30 de maio de 1999")+7 ed.)
  
Retornará 6.
  
## <a name="example-3"></a>Exemplo 3

MONTH(35580.6337)
  
Retornará 5.
  

