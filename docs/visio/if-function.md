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
description: Retorna valueiftrue se logicaly for TRUE. Caso contrário, retornará valueiffalse.
ms.openlocfilehash: 8780bd3dd5ded1a950a5bf3f79333687f3b6843c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405468"
---
# <a name="if-function"></a>Função IF

Retorna _valueiftrue_ se _logicaly_ for true. Caso contrário, retornará _valueiffalse_.
  
## <a name="syntax"></a>Sintaxe

IF (* * *LogicalName* * *, * * *valueiftrue* * *, * * *valueiffalse* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> |Expressão a ser avaliada.  <br/> |
| _valueiftrue_ <br/> |Obrigatório  <br/> |**Vai** <br/> |Valor a ser retornado __ se logicalid for true.  <br/> |
| _valueiffalse_ <br/> |Obrigatório  <br/> |**Vai** <br/> | Valor a ser retornado __ se logicalid for false.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Várias
  
## <a name="example"></a>Exemplo

SE (altura \> 1,25, 5, 7)
  
Retorna 5 se a altura da forma for maior que 1,25 polegadas. Retorna 7 se a altura da forma for menor que ou igual a 1,25 polegadas.
  

