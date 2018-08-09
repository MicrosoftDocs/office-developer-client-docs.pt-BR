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
ms.openlocfilehash: 7fcfd625b5e4e3da71a1b160c074401b672e0be7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771675"
---
# <a name="datevalue-function-visioshapesheet"></a>Função DATEVALUE (VisioShapeSheet)

Retorna o valor de data representado por _datetime_ ou _expression_.
  
## <a name="syntax"></a>Sintaxe

DATEVALUE ("* * *datetime* * *" | * * *expressão* * * [, * * *lcid* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obrigatório  <br/> |**String** <br/> |Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.  <br/> |
| _expressão_ <br/> |Obrigatório  <br/> |**String** <br/> |Qualquer expressão que gere data e hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> |Especifica o identificador de local para ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Datetime
  
## <a name="remarks"></a>Comentários

Qualquer componente de hora em *datetime* ou *expression* é desconsiderado. 
  
Se *datetime* estiver faltando ou não puder ser convertida para um resultado válido, DATEVALUE retornará um #VALUE! erro. 
  
O valor retornado é exibido usando o estilo de data curta definido pelas Configurações regionais atuais do sistema. 
  
A função DATEVALUE também aceita um valor de número único para *expression* em que a parte inteira do resultado representa os dias desde 30 de dezembro de 1899. 
  
## <a name="example-1"></a>Exemplo 1

DATEVALUE(AGORA( ))+5 ed.
  
Retornará a data cinco dias a partir de hoje.
  
## <a name="example-2"></a>Exemplo 2

DATEVALUE("19/07/1995 12:30")
  
Retornará a data.
  
## <a name="example-3"></a>Exemplo 3

DATEVALUE("33 de maio de 1997")
  
Retornará um erro de #VALUE!.
  
## <a name="example-4"></a>Exemplo 4

DATEVALUE(35580.6337)
  
Retornará 30/5/1997.
  

