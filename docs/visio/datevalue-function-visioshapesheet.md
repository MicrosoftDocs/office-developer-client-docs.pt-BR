---
title: Função DATEVALUE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251414
localization_priority: Normal
ms.assetid: 514a4053-7729-ec82-c42f-5b780e48cd2a
description: Retorna o valor de data representado por datetime ou expression.
ms.openlocfilehash: d5bc1865e76940508ddb67a9b3d2122dc7c43a50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360309"
---
# <a name="datevalue-function-visioshapesheet"></a>Função DATEVALUE (VisioShapeSheet)

Retorna o valor de data representado por _datetime_ ou _expression_.
  
## <a name="syntax"></a>Sintaxe

DATEVALUE(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Obrigatório  <br/> |**String** <br/> |Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula contendo uma data e hora.  <br/> |
| _expression_ <br/> |Obrigatório  <br/> |**String** <br/> |Qualquer expressão que produza uma data e hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> |Especifica o identificador de local para ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Datetime
  
## <a name="remarks"></a>Comentários

Qualquer componente de tempo em *datetime* ou *expression* é descartado. 
  
Se a *datetime* estiver ausente ou não puder ser convertida em um resultado válido, DATEVALUE retornará um erro #VALUE! . 
  
O valor retornado é exibido usando o estilo de data abreviada definido pelas atuais configurações regionais do sistema. 
  
A função DATEVALUE também aceita um valor de número único para *expression* em que a parte inteira do resultado representa os dias desde 30 de dezembro de 1899. 
  
## <a name="example-1"></a>Exemplo 1

DATEVALUE(AGORA( ))+5 ed.
  
Retornará a data cinco dias a partir de hoje.
  
## <a name="example-2"></a>Exemplo 2

DATEVALUE("19/07/1995 12:30")
  
Retornará a data.
  
## <a name="example-3"></a>Exemplo 3

DATEVALUE("33 de maio de 1997")
  
Retornar um erro #VALUE!.
  
## <a name="example-4"></a>Exemplo 4

DATEVALUE(35580.6337)
  
Retornará 30/5/1997.
  

