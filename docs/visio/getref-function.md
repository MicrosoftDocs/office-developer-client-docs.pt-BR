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
ms.openlocfilehash: 454314b1f156f560c237f22a45492978ca3c31ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771962"
---
# <a name="getref-function"></a>Função GETREF

Faz referência a uma célula e não recalcula a fórmula quando a célula referenciada é alterada.
  
## <a name="syntax"></a>Sintaxe

GETREF (* * *nome da célula* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _nome da célula_ <br/> |Obrigatório  <br/> |**String** <br/> |O nome da célula para fazer referência à.  <br/> |
   
## <a name="example"></a>Exemplo

SETF(GETREF(PinX),5.1) 
  
Define a fórmula da célula PinX para 5,1. 
  

