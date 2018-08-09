---
title: Função DEPENDSON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251420
localization_priority: Normal
ms.assetid: 8fcfcfdd-69e2-b061-fdb6-d29389d14403
description: Cria uma dependência de referência de célula.
ms.openlocfilehash: 07c0d79668230cbf2b1e8d51b50e67835c87e2f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771704"
---
# <a name="dependson-function"></a>Função DEPENDSON

Cria uma dependência de referência de célula.
  
## <a name="syntax"></a>Sintaxe

DEPENDSON (* * *cellref* * * [, * * *cellref2* * *,...]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _CellRef_ <br/> |Obrigatório  <br/> |**String** <br/> |A referência da primeira célula.  <br/> |
| _cellref2_ <br/> |Opcional  <br/> |**String** <br/> |A referência da segunda célula.  <br/> |
   
## <a name="remarks"></a>Comentários

Essa função sempre retornará FALSO. Ela não tem efeito quando utilizada em uma linha Event ou em uma célula Action. 
  
## <a name="example"></a>Exemplo

OPENTEXTWIN() + DEPENDSON(PinX,PinY) 
  
Abre o bloco de texto para uma forma sempre que as células PinX ou PinY da forma forem alteradas. 
  

