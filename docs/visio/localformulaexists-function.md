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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433287"
---
# <a name="localformulaexists-function"></a>Função LOCALFORMULAEXISTS

Indica se a célula referenciada contém uma fórmula local. 
  
## <a name="syntax"></a>Sintaxe

LOCALFORMULAEXISTS (* * *cellref* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _cellref_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> | A célula cuja presença de fórmula você deseja verificar.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Booliano
  
## <a name="remarks"></a>Comentários

A função LOCALFORMULAEXISTS retornará 1 se a célula contiver uma fórmula local; se não houver fórmula ou se a fórmula for herdada, retornará 0 (zero). 
  

