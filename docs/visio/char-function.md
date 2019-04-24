---
title: Função CHAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251406
localization_priority: Normal
ms.assetid: 0803d5d3-d804-5ffe-604d-661b35d1fc01
description: Retorna o caractere ANSI para um número.
ms.openlocfilehash: 6f1c459892331ec30ad93bbc860fcd038e8f4732
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341906"
---
# <a name="char-function"></a>Função CHAR

Retorna o caractere ANSI para um número.
  
## <a name="syntax"></a>Sintaxe

CARACTERE (* * *número* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Número** <br/> |O número cujo caractere ANSI você deseja obter.  <br/> |
   
## <a name="remarks"></a>Comentários

A cadeia de caracteres resultante é um caractere. O parâmetro _Number_ deve ser um inteiro entre 1 e 255 (inclusive) ou a função retorna um erro. 
  
## <a name="example"></a>Exemplo

CARACTERE (9) 
  
Retornará o caractere de tabulação. 
  

