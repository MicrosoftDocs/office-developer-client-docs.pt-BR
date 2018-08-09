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
ms.openlocfilehash: 4390e0cdccf0ae7798d5ada4329a28f72566ecac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773159"
---
# <a name="time-function-visioshapesheet"></a>Função TIME (VisioShapeSheet)

Retorna a hora representada por _hora_, _minuto_e _segundo_.
  
## <a name="syntax"></a>Sintaxe

TEMPO (* * *hora* * *, * * *minuto* * *, * * *segundo* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _hora_ <br/> |Obrigatório  <br/> |**Numérico** <br/> |O componente de hora.  <br/> |
| _minuto_ <br/> |Obrigatório  <br/> |**Numérico** <br/> |O componente de minuto.  <br/> |
| _segundo_ <br/> |Obrigatório  <br/> |**Numérico** <br/> |O componente de segundo.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Numérico
  
## <a name="example-1"></a>Exemplo 1

TIME(15,30,30)
  
Retornará o valor que representa 15:30:30.
  
## <a name="example-2"></a>Exemplo 2

FORMAT(TIME(15,30,30),"HH:mm")
  
Retornará o valor que representa 15:30.
  
## <a name="example-3"></a>Exemplo 3

TIME(15,30,30) + 8 eh.
  
Retornará o valor que representa 23:30:30.
  

