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
ms.openlocfilehash: 2da084f685c044d48495b04f727a877140b51004
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360316"
---
# <a name="datetime-function"></a>Função DATETIME

Retorna o valor de data e hora representado por _datetime_ ou _expression_.
  
## <a name="syntax"></a>Sintaxe

DATETIME(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Obrigatório  <br/> |**String** <br/> |Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula contendo uma data e hora.  <br/> |
| _expression_ <br/> |Obrigatório  <br/> |**String** <br/> |Qualquer expressão que produza uma data e hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> |Especifica o identificador de local para ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Datetime
  
## <a name="remarks"></a>Comentários

Se a *datetime* estiver faltando ou não puder ser interpretada como uma data ou hora válida, DATETIME retornará um #VALUE! . 
  
O valor retornado é formatado de acordo com o estilo de hora e data abreviada das atuais Configurações Regionais do sistema. 
  
A função DATETIME também aceita um valor de número único para a *expression* em que a parte inteira do resultado representa o número de dias desde 30 de dezembro de 1899 e a parte decimal representa a fração de um dia desde a meia-noite. 
  
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
  

