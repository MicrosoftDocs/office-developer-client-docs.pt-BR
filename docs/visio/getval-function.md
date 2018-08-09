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
ms.openlocfilehash: b4c8ea14b7184101a360c9f5ee4af03fd178aa6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771964"
---
# <a name="getval-function"></a>Função GETVAL

Obtém o valor de uma célula e não recalcula a fórmula quando o valor da célula é alterado.
  
## <a name="syntax"></a>Sintaxe

GETVAL (* * *nome da célula* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _nome da célula_ <br/> |Obrigatório  <br/> |**String** <br/> |O nome da célula de onde obter o valor.  <br/> |
   
## <a name="example"></a>Exemplo

GETVAL(PinX) + GETVAL(PinY) + Width 
  
Retorna a soma do valor das células PinX, PinY e Width. 
  

