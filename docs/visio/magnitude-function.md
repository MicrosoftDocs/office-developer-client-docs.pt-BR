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
description: Retorna a magnitude do vetor cujo aumento é A e cuja execução é B, multiplicada pelas constantes constantA e constantB.
ms.openlocfilehash: 6393c7827e2553ca4948c8b9c51075ca8e4783bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317812"
---
# <a name="magnitude-function"></a>Função MAGNITUDE

Retorna a magnitude do vetor cujo aumento é _a_ e cuja execução é _B_, multiplicada pelas constantes _constantA_ e _constantB_. 
  
## <a name="syntax"></a>Sintaxe

MAGNITUDE (* * *constantA* * *, * * *A* * *, * * *constantB* * *, * * *B* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _constantA_ <br/> |Obrigatório  <br/> |**Número** <br/> |A constante pela qual multiplicar a elevação.  <br/> |
| _A_ <br/> |Obrigatório  <br/> |**Número** <br/> |A elevação.  <br/> |
| _constantB_ <br/> |Obrigatório  <br/> |**Número** <br/> |A constante pela qual multiplicar a execução.  <br/> |
| _A.b.c._ <br/> |Obrigatório  <br/> |**Número** <br/> |A execução.  <br/> |
   
## <a name="remarks"></a>Comentários

MAGNITUDE é calculada de acordo com a fórmula a seguir:
  
SQRT ((constantA \* A) ^ 2 + (constantB \* B) ^ 2)
  
## <a name="example"></a>Exemplo

MAGNITUDE(1, 3, 1, 4) 
  
Retornará 5. 
  

