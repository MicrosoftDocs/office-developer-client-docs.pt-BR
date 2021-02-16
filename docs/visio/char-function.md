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
description: Retorna o caractere ANSI de um número.
ms.openlocfilehash: 6f1c459892331ec30ad93bbc860fcd038e8f4732
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418187"
---
# <a name="char-function"></a>Função CHAR

Retorna o caractere ANSI de um número.
  
## <a name="syntax"></a>Sintaxe

CHAR(** *number* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Número** <br/> |O número cujo caractere ANSI você deseja obter.  <br/> |
   
## <a name="remarks"></a>Comentários

A cadeia de caracteres resultante é um caractere. O  _parâmetro_ number deve ser um número inteiro entre 1 e 255 (inclusive) ou a função retornará um erro. 
  
## <a name="example"></a>Exemplo

CHAR(9) 
  
Retornará o caractere de tabulação. 
  

