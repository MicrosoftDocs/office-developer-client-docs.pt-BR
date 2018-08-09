---
title: Função NOT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251469
localization_priority: Normal
ms.assetid: 65873b32-2406-7c33-8e68-802461f467b2
description: Retorna verdadeiro (1) se logicalexpression for FALSE. Caso contrário, ele retornará FALSE (0).
ms.openlocfilehash: e2359aaab18469cd4f272f71aca8d899a12b2120
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772419"
---
# <a name="not-function"></a>Função NOT

Retorna verdadeiro (1) se _logicalexpression_ for FALSE. Caso contrário, ele retornará FALSE (0). 
  
## <a name="syntax"></a>Sintaxe

NÃO (* * *logicalexpression* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |Obrigatório  <br/> |**String** <br/> |A expressão lógica a ser avaliada.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Booliano
  
## <a name="example"></a>Exemplo

NÃO (altura \> 0,75 pol) 
  
Retorna 1 se a Altura for menor que ou igual a 0,75 polegadas. Retorna 0 se a Altura for maior que 0,75 polegadas. 
  

