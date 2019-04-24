---
title: Função BITAND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251398
localization_priority: Normal
ms.assetid: c437de23-d2e0-469d-62e6-8eb8b8cfea5c
description: Retorna um número binário de 16 bits em que cada bit é definido como 1 somente se o bit correspondente em ambos binarynumber1 e binarynumber2 for 1. Caso contrário, o bit será definido como 0.
ms.openlocfilehash: 495ad645a422c0333d02a22c3c600dd1e0d567bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284466"
---
# <a name="bitand-function"></a>Função BITAND

Retorna um número binário de 16 bits em que cada bit é definido como 1 somente se o bit correspondente em ambos binarynumber1 e binarynumber2 for 1. Caso contrário, o bit será definido como 0. 
  
## <a name="syntax"></a>Sintaxe

BITAND (* * *binarynumber1* * *, * * *binarynumber2* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _Número1 binário_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |O primeiro número binário de 16 bits.  <br/> |
| _número2 binário_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |O segundo número binário de 16 bits.  <br/> |
   
## <a name="remarks"></a>Comentários

É possível usar esta função para testar e alterar propriedades de uma forma armazenadas como bitmasks, por exemplo, o formato do texto da célula.
  
## <a name="example"></a>Exemplo

BITAND (12, 6)
  
Retornará 4. Se 12 = 0...01100 e 6 = 0...00110; consequentemente, BITAND(12,6) = 0...00100.
  

