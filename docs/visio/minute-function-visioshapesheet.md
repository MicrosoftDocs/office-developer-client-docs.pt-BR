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
description: Retorna um inteiro de 0 a 59 que representa o componente de minutos de data e hora ou expressão.
ms.openlocfilehash: 35fe1dc8d4026dd6c829a38504d9ba82d64edda2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436563"
---
# <a name="minute-function-visioshapesheet"></a>Função MINUTE (VisioShapeSheet)

Retorna um inteiro de 0 a 59 que representa o componente de minutos de *data e hora* ou *expressão.* 
  
## <a name="syntax"></a>Sintaxe

MINUTE(" *datetime*  "|  *expressão*  [,  *lcid*  ]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Obrigatório  <br/> |**String** <br/> |Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula contendo uma data e hora.  <br/> |
| _expression_ <br/> |Obrigatório  <br/> |**String** <br/> | Qualquer expressão que produza uma data e hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> |O identificador de local a ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Inteiro
  
## <a name="remarks"></a>Comentários

O componente de data na  _data e_  _na expressão_ é descartado. 
  
Não são feitos arredondamentos. Se _datetime_ estiver faltando ou não puder ser convertida para um resultado válido, a função retornará um erro. 
  
O valor retornado é formatado de acordo com o estilo de hora definido pelas Configurações Regionais atuais do sistema.
  
A função MINUTE também aceita um  valor de número único para a expressão em que a parte decimal representa a fração de um dia desde a meia-noite. 
  
## <a name="example-1"></a>Exemplo 1

MINUTE("7/7/1999 13:45:24")
  
Retornará 45.
  
## <a name="example-2"></a>Exemplo 2

MINUTE(TIMEVALUE("25 de jan. de 1999 12:07:45")+6 em.)
  
Retornará 13.
  
## <a name="example-3"></a>Exemplo 3

MINUTE(0,575)
  
Retornará 48.
  

