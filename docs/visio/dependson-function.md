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
ms.openlocfilehash: 26e7f5fb0620a5f1812d878f02d5bedd43afe524
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360226"
---
# <a name="dependson-function"></a>Função DEPENDSON

Cria uma dependência de referência de célula.
  
## <a name="syntax"></a>Sintaxe

DEPENDSON(** *cellref* ** [, ** *cellref2* **,...]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _cellref_ <br/> |Obrigatório  <br/> |**String** <br/> |A primeira referência de célula.  <br/> |
| _cellref2_ <br/> |Opcional  <br/> |**String** <br/> |A referência da segunda célula.  <br/> |
   
## <a name="remarks"></a>Comentários

Essa função sempre retornará FALSO. Ela não tem efeito quando utilizada em uma linha Event ou em uma célula Action. 
  
## <a name="example"></a>Exemplo

OPENTEXTWIN() + DEPENDSON(PinX,PinY) 
  
Abre o bloco de texto para uma forma sempre que as células PinX ou PinY da forma forem alteradas. 
  

