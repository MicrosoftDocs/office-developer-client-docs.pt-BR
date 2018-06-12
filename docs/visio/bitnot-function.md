---
title: Função BITNOT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251399
localization_priority: Normal
ms.assetid: 7b6486bb-3618-3747-4b00-93bd55767c1c
description: Retorna um número binário de 16 bits no qual cada bit for definido como 1 somente se o bit correspondente no número binário for 0. Caso contrário, o bit é definido como 0.
ms.openlocfilehash: 0806e7c52cab659a09d27a60efb9c09aa436fb92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771340"
---
# <a name="bitnot-function"></a>Função BITNOT

Retorna um número binário de 16 bits no qual cada bit for definido como 1 somente se o bit correspondente no número binário for 0. Caso contrário, o bit é definido como 0.
  
## <a name="syntax"></a>Sintaxe

BITNOT (* * *número binário* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _número binário_ <br/> |Obrigatório  <br/> |**Numérico** <br/> |Um número binário de 16 bits.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Binário de 16 bits
  
## <a name="example"></a>Example

BITNOT(6)
  
Retornará 65529. Se 6 = 0...00110; consequentemente, BITNOT(6) = 1...11001.
  

