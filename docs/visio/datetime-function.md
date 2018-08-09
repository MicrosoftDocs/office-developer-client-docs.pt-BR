---
title: Função DATETIME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251413
localization_priority: Normal
ms.assetid: 0bf7f757-0b7f-dec1-9709-6612c9ad0d53
description: Retorna o valor de data e hora representado por datetime ou expression.
ms.openlocfilehash: 001430acaf9fcb670e95157380e474e12b9728cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771677"
---
# <a name="datetime-function"></a>Função DATETIME

Retorna o valor de data e hora representado por _datetime_ ou _expression_.
  
## <a name="syntax"></a>Sintaxe

DATETIME ("* * *datetime* * *" | * * *expressão* * * [, * * *lcid* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obrigatório  <br/> |**String** <br/> |Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.  <br/> |
| _expressão_ <br/> |Obrigatório  <br/> |**String** <br/> |Qualquer expressão que gere data e hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> |Especifica o identificador de local para ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Datetime
  
## <a name="remarks"></a>Comentários

Se *datetime* estiver faltando ou não puder ser interpretada como uma data ou hora válida, DATETIME retornará um #VALUE! erro. 
  
O valor retornado é formatado de acordo com o estilo de data e hora curtas nas Configurações regionais do sistema. 
  
A função DATETIME também aceita um valor de número único para *expression* em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899 e a parte decimal representa a fração de um dia desde a meia-noite. 
  
## <a name="example-1"></a>Exemplo 1

DATETIME("30 de maio de 1997")+5 ed.
  
Retornará o valor que representa 04/06/97.
  
## <a name="example-2"></a>Exemplo 2

FORMAT(DATETIME("20/05/1997 14:30:45"),"C")
  
Retornará a sequência de caracteres "Terça-feira, 20 de maio de 1997, 14:30:45."
  
## <a name="example-3"></a>Exemplo 3

DATETIME("13:30 19 de julho")
  
Retornará o valor que representa 19/07/2001 13:30 (partindo do pressuposto que o ano atual seja 2001).
  
## <a name="example-4"></a>Exemplo 4

DATETIME(35580.6337)
  
Retornará o valor representando 30/5/1997 3:12:32 PM.
  

