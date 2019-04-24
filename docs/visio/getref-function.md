---
title: Função GETREF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251884
localization_priority: Normal
ms.assetid: 25c9f817-d22b-28c9-1339-dc9f27d0dd41
description: Faz referência a uma célula e não recalcula a fórmula quando a célula referenciada é alterada.
ms.openlocfilehash: 38f3c8b4f34ed2b3d3711be5faed6b0d317e907a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356492"
---
# <a name="getref-function"></a>Função GETREF

Faz referência a uma célula e não recalcula a fórmula quando a célula referenciada é alterada.
  
## <a name="syntax"></a>Sintaxe

GETREF (* * *cellname* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _cellname_ <br/> |Obrigatório  <br/> |**String** <br/> |O nome da célula para obter uma referência.  <br/> |
   
## <a name="example"></a>Exemplo

SETF (GETREF (PinX), 5.1) 
  
Define a fórmula da célula PinX para 5,1. 
  

