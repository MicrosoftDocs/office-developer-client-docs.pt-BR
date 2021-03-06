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
description: Retorna a magnitude do vetor cuja elevação é A e cujo fluxo é B, multiplicado pelas constantes respectivas constantA e constantB.
ms.openlocfilehash: 6393c7827e2553ca4948c8b9c51075ca8e4783bd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420455"
---
# <a name="magnitude-function"></a>Função MAGNITUDE

Retorna a magnitude do vetor cuja elevação é  _A_ e cujo fluxo é  _B_, multiplicado pelas constantes  _respectivas constantA_ e  _constantB_. 
  
## <a name="syntax"></a>Sintaxe

MAGNITUDE(** *constantA* **, ** *A* **, ** *constantB* **, ** *B* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _constantA_ <br/> |Obrigatório  <br/> |**Número** <br/> |A constante pela qual multiplicar a elevação.  <br/> |
| _A_ <br/> |Obrigatório  <br/> |**Número** <br/> |A elevação.  <br/> |
| _constantB_ <br/> |Obrigatório  <br/> |**Número** <br/> |A constante pela qual multiplicar a execução.  <br/> |
| _B_ <br/> |Obrigatório  <br/> |**Número** <br/> |A execução.  <br/> |
   
## <a name="remarks"></a>Comentários

MAGNITUDE é calculada de acordo com a fórmula a seguir:
  
SQRT((constantA \* A)^2 + (constantB \* B)^2)
  
## <a name="example"></a>Exemplo

MAGNITUDE(1, 3, 1, 4) 
  
Retornará 5. 
  

