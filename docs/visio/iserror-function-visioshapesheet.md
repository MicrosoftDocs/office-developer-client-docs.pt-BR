---
title: Função ISERROR (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251452
localization_priority: Normal
ms.assetid: 4864ebc2-fee6-2415-7c59-e0af8611f8d6
description: Retorna TRUE se o valor de cellreference for qualquer tipo de erro; caso contrário, retornará FALSE. A função isERROr é usada em fórmulas que se referem a outra célula.
ms.openlocfilehash: a07b2345858e36dc2e4514d7e4f0f0d653491b50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317887"
---
# <a name="iserror-function-visioshapesheet"></a>Função ISERROR (VisioShapeSheet)

Retorna TRUE se o valor de _cellreference_ for qualquer tipo de erro; caso contrário, retornará FALSE. A função isERROr é usada em fórmulas que se referem a outra célula. 
  
## <a name="syntax"></a>Sintaxe

IsERROr (* * *cellreference* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Obrigatório  <br/> |**String** <br/> |Referência a uma célula.  <br/> |
   
## <a name="example-1"></a>Exemplo 1

|**Cell**|**Fórmula**|**Valor retornado**|
|:-----|:-----|:-----|
|Scratch. a1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch. B1  <br/> |= IsERROr (Scratch. a1)  <br/> |TRUE  <br/> |
   
Retornará VERDADEIRO porque o erro de #N/A! é reconhecido pela função ISERROR. Utilize a função ISERR para localizar todos os tipos de erro, exceto #N/A!.
  
## <a name="example-2"></a>Exemplo 2

|**Cell**|**Fórmula**|**Valor retornado**|
|:-----|:-----|:-----|
|Scratch. X1  <br/> |= "House"  <br/> |#VALUE!  <br/> |
|Scratch. B1  <br/> |= IsERROr (Scratch. X1)  <br/> |TRUE  <br/> |
   
Retornará VERDADEIRO porque o erro de #VALUE! é reconhecido pela função ISERROR. Para criar uma expressão com base no erro de #VALUE!, utilize a função ISERRVALUE.
  

