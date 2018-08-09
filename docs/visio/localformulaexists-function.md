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
ms.openlocfilehash: 1b749011de8554cb5b777fe92b20a6bcdb2fcb19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772237"
---
# <a name="localformulaexists-function"></a>Função LOCALFORMULAEXISTS

Indica se a célula referenciada contém uma fórmula local. 
  
## <a name="syntax"></a>Sintaxe

LOCALFORMULAEXISTS (* * *cellref* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _CellRef_ <br/> |Obrigatório  <br/> |**String** <br/> | A célula cuja presença de fórmula você deseja verificar.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Booliano
  
## <a name="remarks"></a>Comentários

A função LOCALFORMULAEXISTS retornará 1 se a célula contiver uma fórmula local; se não houver fórmula ou se a fórmula for herdada, retornará 0 (zero). 
  

