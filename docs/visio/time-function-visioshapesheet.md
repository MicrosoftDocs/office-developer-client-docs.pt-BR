---
title: Função TIME (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
localization_priority: Normal
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: Retorna a hora representada por hora, minuto e segundo.
ms.openlocfilehash: f5be55d7e63a70d15da49c68b924cc5b03c5ca88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280994"
---
# <a name="time-function-visioshapesheet"></a>Função TIME (VisioShapeSheet)

Retorna a hora representada por _hora_, _minuto_e _segundo_.
  
## <a name="syntax"></a>Sintaxe

HORA (* * *hora* * *, * * *minuto* * *, * * *segundo* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _hora_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |O componente de hora.  <br/> |
| _inclusões_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |O componente de minuto.  <br/> |
| _secundária_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |O componente de segundo.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Numeric
  
## <a name="example-1"></a>Exemplo 1

TEMPO (15, 30, 30)
  
Retornará o valor que representa 15:30:30.
  
## <a name="example-2"></a>Exemplo 2

FORMATO (tempo (15, 30, 30), "HH: mm")
  
Retornará o valor que representa 15:30.
  
## <a name="example-3"></a>Exemplo 3

TIME(15,30,30) + 8 eh.
  
Retornará o valor que representa 23:30:30.
  

