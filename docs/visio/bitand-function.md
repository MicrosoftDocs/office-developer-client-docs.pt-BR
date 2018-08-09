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
description: Retorna um número binário de 16 bits no qual cada bit for definido como 1 somente se o bit correspondente em númerobinário1 e númerobinário2 é 1. Caso contrário, o bit é definido como 0.
ms.openlocfilehash: 0b501bb383596e3f2f39ea14f2cb9eb4bf40b25b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771365"
---
# <a name="bitand-function"></a>Função BITAND

Retorna um número binário de 16 bits no qual cada bit for definido como 1 somente se o bit correspondente em númerobinário1 e númerobinário2 é 1. Caso contrário, o bit é definido como 0. 
  
## <a name="syntax"></a>Sintaxe

BITAND (* * *númerobinário1* * *, * * *númerobinário2* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _Número1 binários_ <br/> |Obrigatório  <br/> |**Numérico** <br/> |O primeiro número binário de 16 bits.  <br/> |
| _binário 2_ <br/> |Obrigatório  <br/> |**Numérico** <br/> |O segundo número binário de 16 bits.  <br/> |
   
## <a name="remarks"></a>Comentários

É possível usar esta função para testar e alterar propriedades de uma forma armazenadas como bitmasks, por exemplo, o formato do texto da célula.
  
## <a name="example"></a>Exemplo

BITAND(12,6)
  
Retornará 4. Se 12 = 0...01100 e 6 = 0...00110; consequentemente, BITAND(12,6) = 0...00100.
  

