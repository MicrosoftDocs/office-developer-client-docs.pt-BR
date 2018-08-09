---
title: Função MAGNITUDE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251461
localization_priority: Normal
ms.assetid: 9f443687-9861-5f51-94c4-f056805f736b
description: Retorna a magnitude do vetor cuja elevação é A e cuja execução é B, multiplicada pelas constantes constanteA e constanteB.
ms.openlocfilehash: f4c428b8b381af58958dab66a71ddd0bcaf715c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772304"
---
# <a name="magnitude-function"></a>Função MAGNITUDE

Retorna a magnitude do vetor cuja elevação é _A_ e cuja execução é _B_, multiplicada pelas respectivas constantes _constanteA_ e _constanteB_. 
  
## <a name="syntax"></a>Sintaxe

MAGNITUDE (* * *constanteA* * *, * * *uma* * *, * * *constanteB* * *, * * *B* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _constanteA_ <br/> |Obrigatório  <br/> |**Número** <br/> |A constante pela qual multiplicar a elevação.  <br/> |
| _A_ <br/> |Obrigatório  <br/> |**Número** <br/> |A elevação.  <br/> |
| _constanteB_ <br/> |Obrigatório  <br/> |**Número** <br/> |A constante pela qual multiplicar a execução.  <br/> |
| _B_ <br/> |Obrigatório  <br/> |**Número** <br/> |A execução.  <br/> |
   
## <a name="remarks"></a>Comentários

MAGNITUDE é calculada de acordo com a fórmula a seguir:
  
SQRT ((constanteA \* uma) ^ 2 + (constanteB \* B) ^ 2)
  
## <a name="example"></a>Exemplo

MAGNITUDE(1, 3, 1, 4) 
  
Retornará 5. 
  

