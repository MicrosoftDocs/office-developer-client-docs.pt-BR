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
description: Retorna o tempo representado por hora, minuto e segundo.
ms.openlocfilehash: f5be55d7e63a70d15da49c68b924cc5b03c5ca88
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414470"
---
# <a name="time-function-visioshapesheet"></a>Função TIME (VisioShapeSheet)

Retorna o tempo representado por _hora,_ _minuto_ e _segundo._
  
## <a name="syntax"></a>Sintaxe

TIME(** *hour* **, ** *minute* **, ** *second* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _hour_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O componente de hora.  <br/> |
| _minute_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O componente de minuto.  <br/> |
| _segundo_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O componente de segundo.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Numeric
  
## <a name="example-1"></a>Exemplo 1

TIME(15,30,30)
  
Retornará o valor que representa 15:30:30.
  
## <a name="example-2"></a>Exemplo 2

FORMAT(TIME(15,30,30),"HH:mm")
  
Retornará o valor que representa 15:30.
  
## <a name="example-3"></a>Exemplo 3

TIME(15,30,30) + 8 eh.
  
Retornará o valor que representa 23:30:30.
  

