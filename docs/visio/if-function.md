---
title: Função IF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251442
localization_priority: Normal
ms.assetid: 66771ad3-0fb3-68ff-81da-d1162d37c05a
description: Retorna ValorSeVerdadeiro se logicalexpression for TRUE. Caso contrário, ele retorna ValorSeFalso.
ms.openlocfilehash: 55938e8bd78c02badb98f90665c5c26cdd70f3b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772056"
---
# <a name="if-function"></a>Função IF

Retorna _ValorSeVerdadeiro_ se _logicalexpression_ for TRUE. Caso contrário, ele retorna _ValorSeFalso_.
  
## <a name="syntax"></a>Sintaxe

IF (* * *logicalexpression* * *, * * *ValorSeVerdadeiro* * *, * * *ValorSeFalso* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |Obrigatório  <br/> |**String** <br/> |Expressão a ser avaliada.  <br/> |
| _ValorSeVerdadeiro_ <br/> |Obrigatório  <br/> |**Varia** <br/> |O valor retornado se _logicalexpression_ for true.  <br/> |
| _ValorSeFalso_ <br/> |Obrigatório  <br/> |**Varia** <br/> | O valor retornado se _logicalexpression_ for falso.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Varia
  
## <a name="example"></a>Exemplo

IF (altura \> 1,25 pol, 5, 7)
  
Retorna 5 se a altura da forma for maior que 1,25 polegadas. Retorna 7 se a altura da forma for menor que ou igual a 1,25 polegadas.
  

