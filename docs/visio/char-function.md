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
ms.openlocfilehash: 209614d20dd663ed2f7ca030c25500d43f925c95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771479"
---
# <a name="char-function"></a>Função CHAR

Retorna o caractere ANSI para um número.
  
## <a name="syntax"></a>Sintaxe

CHAR (* * *número* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Número** <br/> |O número de caractere ANSI você deseja obter.  <br/> |
   
## <a name="remarks"></a>Comentários

A cadeia de caracteres resultante é um caractere de comprimento. O parâmetro _número_ deve ser um inteiro entre 1 e 255 (inclusive) ou a função retornará um erro. 
  
## <a name="example"></a>Exemplo

CHAR(9) 
  
Retornará o caractere de tabulação. 
  

