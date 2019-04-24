---
title: Função LOCALFORMULAEXISTS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60105
localization_priority: Normal
ms.assetid: 2b757c8d-7732-0f9b-c836-ef755dd1c673
description: Indica se a célula referenciada contém uma fórmula local.
ms.openlocfilehash: bd0a5dafecf1bd8dca1567392d880ecaaa3e0374
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344461"
---
# <a name="localformulaexists-function"></a>Função LOCALFORMULAEXISTS

Indica se a célula referenciada contém uma fórmula local. 
  
## <a name="syntax"></a>Sintaxe

LOCALFORMULAEXISTS (* * *cellref* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _cellref_ <br/> |Obrigatório  <br/> |**String** <br/> | A célula cuja presença de fórmula você deseja verificar.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Booliano
  
## <a name="remarks"></a>Comentários

A função LOCALFORMULAEXISTS retornará 1 se a célula contiver uma fórmula local; se não houver fórmula ou se a fórmula for herdada, retornará 0 (zero). 
  

