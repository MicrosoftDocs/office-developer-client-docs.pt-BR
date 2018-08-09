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
description: 'Retornará TRUE se o valor de referênciadecélula for erro digite #VALUE, onde um argumento na fórmula é do tipo incorreto. A função ISERRVALUE é usada em expressões lógicas que se referem a outra célula.'
ms.openlocfilehash: 50c501cc404d9c5f80e0bd1261b3d3bcd7087de2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772115"
---
# <a name="iserrvalue-function"></a>Função ISERRVALUE

Retornará TRUE se o valor de _referênciadecélula_ for erro digite #VALUE, onde um argumento na fórmula é do tipo incorreto. A função ISERRVALUE é usada em expressões lógicas que se referem a outra célula. 
  
## <a name="syntax"></a>Sintaxe

ISERRVALUE (* * *referênciadecélula* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _referênciadecélula_ <br/> |Obrigatório  <br/> |**String** <br/> |Referência a uma célula.  <br/> |
   
## <a name="remarks"></a>Comentários

As células transitórias de A a D não retornarão um erro de #VALUE! porque a fórmula pode conter números e letras na mesma sequência de caracteres. As células X e Y devem conter apenas números. 
  
## <a name="example-1"></a>Exemplo 1

|**Célula**|**Formula**|**Valor retornado**|
|:-----|:-----|:-----|
|Y1  <br/> |="Casa"  <br/> |#VALUE!  <br/> |
|Scratch. a1  <br/> |= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)  <br/> |2  <br/> |
   
Retornará 2 porque o valor retornado é um erro de #VALUE! e a expressão instrui o Microsoft Visio a retornar um 2 no lugar do erro.
  
## <a name="example-2"></a>Exemplo 2

|**Célula**|**Formula**|**Valor retornado**|
|:-----|:-----|:-----|
|Scratch. a1  <br/> |="5 + 7"  <br/> |5 + 7  <br/> |
|Scratch.B1  <br/> |=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)  <br/> |5 + 7  <br/> |
   
Retornará 12 porque o valor retornado não é um erro de #VALUE! e a expressão instrui o Visio a retornar o valor da célula original.
  

