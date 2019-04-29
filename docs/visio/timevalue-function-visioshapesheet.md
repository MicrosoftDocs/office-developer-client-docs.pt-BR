---
title: Função TIMEVALUE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251507
localization_priority: Normal
ms.assetid: 53579e0e-fcec-e745-0207-3861b5efa333
description: Retorna o valor de tempo representado por DateTime ou expressão, com base nas configurações de idioma e região do sistema.
ms.openlocfilehash: 61eeafac64ce199eba0f9032c42474d2b44febce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432321"
---
# <a name="timevalue-function-visioshapesheet"></a>Função TIMEVALUE (VisioShapeSheet)

Retorna o valor de tempo representado por _DateTime_ ou _expressão_, com base nas configurações de idioma e região do sistema.
  
## <a name="syntax"></a>Sintaxe

TIMEvalue ("* * *DateTime* * *" | * * *expressão* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Obrigatório  <br/> |**String** <br/> | Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula contendo uma data e hora.  <br/> |
| _expressão_ <br/> |Obrigatório  <br/> |**Vai** <br/> | Qualquer expressão que produza uma data e hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> |O identificador de local a ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.  <br/> |
   
## <a name="remarks"></a>Comentários

Qualquer componente de data em _DateTime_ ou _expression_ é Descartado. 
  
Se a _data/hora_ estiver ausente ou não puder ser convertida em um resultado válido, essa função retornará um #VALUE! #NUM! 
  
A função TIMEvalue também aceita um valor de número único para _expressão_ em que a parte decimal do resultado representa a fração de um dia desde a meia-noite. 
  
## <a name="example-1"></a>Exemplo 1

TIMEVALUE("6:00")
  
Retornará o valor que representa 06:00.
  
## <a name="example-2"></a>Exemplo 2

TIMEVALUE("14:30")+4 eh.+30 em.
  
Retornará o valor que representa 19:00:00.
  
## <a name="example-3"></a>Exemplo 3

TIMEVALUE("11:00, 1º de julho de 1997")
  
Retornará o valor que representa 11:00.
  
## <a name="example-4"></a>Exemplo 4

TIMEVALUE (0.6337)
  
Retornará o valor que representa 15:12:32.
  
## <a name="example-5"></a>Exemplo 5

TIMEVALUE ("7:89")
  
Retornará um erro de #VALUE!.
  

