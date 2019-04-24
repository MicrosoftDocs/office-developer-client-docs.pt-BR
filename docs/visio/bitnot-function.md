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
description: Retorna um número binário de 16 bits em que cada bit é definido como 1 somente se o bit correspondente no número binário for 0. Caso contrário, o bit será definido como 0.
ms.openlocfilehash: 34ea6fd614feae8e3c8e97e34b7ff6c531f4c123
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330006"
---
# <a name="bitnot-function"></a>Função BITNOT

Retorna um número binário de 16 bits em que cada bit é definido como 1 somente se o bit correspondente no número binário for 0. Caso contrário, o bit será definido como 0.
  
## <a name="syntax"></a>Sintaxe

BITNOT (* * *número binário* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _número binário_ <br/> |Obrigatório  <br/> |**Numeric** <br/> |Um número binário de 16 bits.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Binário de 16 bits
  
## <a name="example"></a>Exemplo

BITNOT (6)
  
Retornará 65529. Se 6 = 0...00110; consequentemente, BITNOT(6) = 1...11001.
  

