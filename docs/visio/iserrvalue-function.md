---
title: Função ISERRVALUE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251453
localization_priority: Normal
ms.assetid: c7feec6f-f47a-60ee-b056-7b2dc51ed9a9
description: 'Retorna TRUE se o valor de cellreference for o tipo de erro #VALUE, onde um argumento na fórmula é do tipo errado. A função ISERRVALUE é usada em expressões lógicas que se referem a outra célula.'
ms.openlocfilehash: 62058522dc8a2387aec9867e4892da740aba9b44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317882"
---
# <a name="iserrvalue-function"></a>Função ISERRVALUE

Retorna TRUE se o valor de _cellreference_ for o tipo de erro #VALUE, onde um argumento na fórmula é do tipo errado. A função ISERRVALUE é usada em expressões lógicas que se referem a outra célula. 
  
## <a name="syntax"></a>Sintaxe

ISERRVALUE (* * *cellreference* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Obrigatório  <br/> |**String** <br/> |Referência a uma célula.  <br/> |
   
## <a name="remarks"></a>Comentários

As células transitórias de A a D não retornarão um erro de #VALUE! porque a fórmula pode conter números e letras na mesma sequência de caracteres. As células X e Y devem conter apenas números. 
  
## <a name="example-1"></a>Exemplo 1

|**Cell**|**Fórmula**|**Valor retornado**|
|:-----|:-----|:-----|
|Scratch. X1  <br/> |="Casa"  <br/> |#VALUE!  <br/> |
|Scratch. a1  <br/> |= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)  <br/> |duas  <br/> |
   
Retornará 2 porque o valor retornado é um erro de #VALUE! e a expressão instrui o Microsoft Visio a retornar um 2 no lugar do erro.
  
## <a name="example-2"></a>Exemplo 2

|**Cell**|**Fórmula**|**Valor retornado**|
|:-----|:-----|:-----|
|Scratch. a1  <br/> |="5 + 7"  <br/> |5 + 7  <br/> |
|Scratch. B1  <br/> |=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)  <br/> |5 + 7  <br/> |
   
Retornará 12 porque o valor retornado não é um erro de #VALUE! e a expressão instrui o Visio a retornar o valor da célula original.
  

