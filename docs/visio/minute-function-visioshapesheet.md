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
description: Retorna um número inteiro entre 0 e 59 que representa o componente de minutos de datetime ou expression.
ms.openlocfilehash: 7c35ec15f2cebd95bb09924ca94f20630c862360
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772397"
---
# <a name="minute-function-visioshapesheet"></a>Função MINUTE (VisioShapeSheet)

Retorna um número inteiro entre 0 e 59 que representa o componente de minutos de *datetime* ou *expression* . 
  
## <a name="syntax"></a>Sintaxe

MINUTO (" *datetime* " |  *expressão*  [, *lcid* ]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obrigatório  <br/> |**String** <br/> |Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.  <br/> |
| _expressão_ <br/> |Obrigatório  <br/> |**String** <br/> | Qualquer expressão que gere data e hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> |O identificador de local a ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Inteiro
  
## <a name="remarks"></a>Comentários

O componente de data em _datetime_ e _expression_ é desconsiderado. 
  
É feito nenhum arredondamento. Se _datetime_ estiver faltando ou não puder ser convertida para um resultado válido, a função retornará um erro. 
  
O valor retornado é formatado de acordo com o estilo de hora definido pelas Configurações Regionais atuais do sistema.
  
A função MINUTE também aceita um valor de número único para _expression_ em que a parte decimal representa a fração de um dia desde a meia-noite. 
  
## <a name="example-1"></a>Exemplo 1

MINUTE("07/07/99 13:45:24")
  
Retornará 45.
  
## <a name="example-2"></a>Exemplo 2

MINUTE(TIMEVALUE("25 de jan. de 1999 12:07:45")+6 em.)
  
Retornará 13.
  
## <a name="example-3"></a>Exemplo 3

MINUTE(0.575)
  
Retornará 48.
  

