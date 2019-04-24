---
title: Função MINUTE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251464
localization_priority: Normal
ms.assetid: 5a90cb16-7eef-8876-8e25-408787b16f58
description: Retorna um inteiro de 0 a 59 que representa o componente de minutos de DateTime ou expressão.
ms.openlocfilehash: 35fe1dc8d4026dd6c829a38504d9ba82d64edda2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283969"
---
# <a name="minute-function-visioshapesheet"></a>Função MINUTE (VisioShapeSheet)

Retorna um inteiro de 0 a 59 que representa o componente de minutos de *DateTime* ou *expressão* . 
  
## <a name="syntax"></a>Sintaxe

MINUTE (" *DateTime* " |  *expressão*  [, *LCID* ]) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obrigatório  <br/> |**String** <br/> |Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.  <br/> |
| _expressão_ <br/> |Obrigatório  <br/> |**String** <br/> | Qualquer expressão que gere data e hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> |O identificador de local a ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Inteiro
  
## <a name="remarks"></a>Comentários

O componente de data em _DateTime_ e _expression_ é Descartado. 
  
Não é feito nenhum arredondamento. Se a _data/hora_ estiver ausente ou não puder ser convertida em um resultado válido, a função retornará um erro. 
  
O valor retornado é formatado de acordo com o estilo de hora definido pelas Configurações Regionais atuais do sistema.
  
A função MINUTE também aceita um valor de número único para _expressão_ em que a parte decimal representa a fração de um dia desde a meia-noite. 
  
## <a name="example-1"></a>Exemplo 1

MINUTE ("7/7/1999 13:45:24")
  
Retornará 45.
  
## <a name="example-2"></a>Exemplo 2

MINUTE(TIMEVALUE("25 de jan. de 1999 12:07:45")+6 em.)
  
Retornará 13.
  
## <a name="example-3"></a>Exemplo 3

MINUTE (0.575)
  
Retornará 48.
  

