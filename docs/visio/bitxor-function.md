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
description: Retorna um número binário de 16 bits em que cada bit é definido como 1 se o bit correspondente em ambos, mas não no número binário e no número binário núm2 é 1. Caso contrário, o bit será definido como 0.
ms.openlocfilehash: ab8ff46fe98512d963ef4ecd5c37127353827725
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302986"
---
# <a name="bitxor-function"></a>Função BITXOR

Retorna um número binário de 16 bits em que cada bit é definido como 1 se o bit correspondente em ambos, mas não no número binário e no número binário núm2 é 1. Caso contrário, o bit será definido como 0.
  
## <a name="syntax"></a>Sintaxe

BITXOR (* * *binário Número1* * *, * * *binário núm2* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _Número1 binário_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |O primeiro número binário de 16 bits.  <br/> |
| _número2 binário_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |O segundo número binário de 16 bits.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Binário de 16 bits
  
## <a name="example"></a>Exemplo

BITXOR (12, 6)
  
Retornará 10. Se 12 = 0...01100 e 6 = 0...00110; consequentemente, BITXOR(12,6) = 0...01010.
  

