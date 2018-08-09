---
title: Função BITXOR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251401
localization_priority: Normal
ms.assetid: 672eacaf-a374-c7e2-b39b-8d42d2371aee
description: Retorna um número binário de 16 bits no qual cada bit for definido como 1 se o bit correspondente em ambos, mas não ambos binário Núm1 e núm2 binário é 1. Caso contrário, o bit é definido como 0.
ms.openlocfilehash: a0e03258bcfe694dc3bec5469095eff90fb94f1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771376"
---
# <a name="bitxor-function"></a>Função BITXOR

Retorna um número binário de 16 bits no qual cada bit for definido como 1 se o bit correspondente em ambos, mas não ambos binário Núm1 e núm2 binário é 1. Caso contrário, o bit é definido como 0.
  
## <a name="syntax"></a>Sintaxe

BITXOR (* * *Número1 binário* * *, * * *binário 2* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _Número1 binários_ <br/> |Obrigatório  <br/> |**Numérico** <br/> |O primeiro número binário de 16 bits.  <br/> |
| _binário 2_ <br/> |Obrigatório  <br/> |**Numérico** <br/> |O segundo número binário de 16 bits.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Binário de 16 bits
  
## <a name="example"></a>Exemplo

BITXOR(12,6)
  
Retornará 10. Se 12 = 0...01100 e 6 = 0...00110; consequentemente, BITXOR(12,6) = 0...01010.
  

