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
description: Retorna um número binário de 16 bits em que cada bit é definido como 1 se o bit correspondente no número binário ou no número binário núm2 for 1. O bit é definido como 0 somente se o bit correspondente for 0 no Número1 binário e no número2 binário.
ms.openlocfilehash: 13bda2c6c65557b1f8372432cf919b2aaf2d75de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303371"
---
# <a name="bitor-function"></a>Função BITOR

Retorna um número binário de 16 bits em que cada bit é definido como 1 se o bit correspondente no número *binário* ou no número *binário núm2* for 1. O bit é definido como 0 somente se o bit correspondente for 0 no *Número1 binário* e no *número2 binário* . 
  
## <a name="syntax"></a>Sintaxe

BITOR (* * *binário Número1* * *, * * *binário núm2* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _Número1 binário_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |O primeiro número binário de 16 bits.  <br/> |
| _número2 binário_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |O segundo número binário de 16 bits.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Binário de 16 bits
  
## <a name="example"></a>Exemplo

BITOR (12, 6)
  
Retornará 14. Se 12 = 0...01100 e 6 = 0...00110; consequentemente, BITOR(12,6) = 0...01110.
  

