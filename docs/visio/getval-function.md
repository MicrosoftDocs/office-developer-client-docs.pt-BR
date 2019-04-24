---
title: Função GETVAL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251885
localization_priority: Normal
ms.assetid: 1da42991-5791-ebab-84cc-286cfe984a61
description: Obtém o valor de uma célula e não recalcula a fórmula quando o valor da célula é alterado.
ms.openlocfilehash: 9449ccd8f849b23faf08ee25826301a1b6efe6d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327311"
---
# <a name="getval-function"></a>Função GETVAL

Obtém o valor de uma célula e não recalcula a fórmula quando o valor da célula é alterado.
  
## <a name="syntax"></a>Sintaxe

GETVAL (* * *cellname* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _cellname_ <br/> |Obrigatório  <br/> |**String** <br/> |O nome da célula de onde obter o valor.  <br/> |
   
## <a name="example"></a>Exemplo

GETVAL(PinX) + GETVAL(PinY) + Width 
  
Retorna a soma do valor das células PinX, PinY e Width. 
  

