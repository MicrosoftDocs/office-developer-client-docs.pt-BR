---
title: Função BITOR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251400
localization_priority: Normal
ms.assetid: 1d0954c5-b2cb-6c5d-62b3-a68011cf0c85
description: Retorna um número binário de 16 bits no qual cada bit for definido como 1 se o bit correspondente em binário Número1 ou Número2 binário é 1. O bit é definido como 0 somente se o bit correspondente for 0 em binário Núm1 e núm2 binário.
ms.openlocfilehash: db9808f16b32776149abbddf882310c02268cec3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771357"
---
# <a name="bitor-function"></a>Função BITOR

Retorna um número binário de 16 bits no qual cada bit for definido como 1 se o bit correspondente em *binário Número1* ou *número2 binário* é 1. O bit é definido como 0 somente se o bit correspondente for 0 em *binário Núm1* e *núm2 binário* . 
  
## <a name="syntax"></a>Sintaxe

BITOR (* * *Número1 binário* * *, * * *binário 2* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _Número1 binários_ <br/> |Obrigatório  <br/> |**Numérico** <br/> |O primeiro número binário de 16 bits.  <br/> |
| _binário 2_ <br/> |Obrigatório  <br/> |**Numérico** <br/> |O segundo número binário de 16 bits.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Binário de 16 bits
  
## <a name="example"></a>Exemplo

BITOR(12,6)
  
Retornará 14. Se 12 = 0...01100 e 6 = 0...00110; consequentemente, BITOR(12,6) = 0...01110.
  

