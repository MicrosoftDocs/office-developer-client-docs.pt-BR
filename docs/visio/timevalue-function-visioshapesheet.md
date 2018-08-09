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
description: Retorna o valor de hora representado por datetime ou expressão, com base no idioma e região do sistema configurações.
ms.openlocfilehash: e75607d19dc7062af717823c13f580cb44c9406b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773145"
---
# <a name="timevalue-function-visioshapesheet"></a>Função TIMEVALUE (VisioShapeSheet)

Retorna o valor de hora representado por _datetime_ ou _expressão_, com base no idioma e região do sistema configurações.
  
## <a name="syntax"></a>Sintaxe

TIMEVALUE ("* * *datetime* * *" | * * *expressão* * * [, * * *lcid* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obrigatório  <br/> |**String** <br/> | Qualquer cadeia de caracteres comumente reconhecida como uma data e hora ou uma referência a uma célula que contém data e hora.  <br/> |
| _expressão_ <br/> |Obrigatório  <br/> |**Varia** <br/> | Qualquer expressão que gere data e hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> |O identificador de local a ser utilizado na avaliação de uma data e hora não locais. O identificador de local é um número descrito nos arquivos de cabeçalho do sistema.  <br/> |
   
## <a name="remarks"></a>Comentários

Qualquer componente de data em _datetime_ ou _expression_ é desconsiderado. 
  
Se _datetime_ estiver faltando ou não puder ser convertida para um resultado válido, essa função retornará um #VALUE! erro. 
  
A função TIMEVALUE também aceita um valor de número único para _expression_ em que a parte decimal do resultado representa a fração de um dia desde a meia-noite. 
  
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

TIMEVALUE(0.6337)
  
Retornará o valor que representa 15:12:32.
  
## <a name="example-5"></a>Exemplo 5

TIMEVALUE("7:89")
  
Retornará um erro de #VALUE!.
  

