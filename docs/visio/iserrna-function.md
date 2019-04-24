---
title: Função ISERRNA
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251451
localization_priority: Normal
ms.assetid: 6ee7dc3d-efe9-c862-f71d-034b3d9c3ec6
description: 'Retorna TRUE se o valor de cellreference for o tipo de erro #N/A! (não disponível); caso contrário, retornará FALSE. A função ISERRNA é usada em fórmulas que se referem a outra célula.'
ms.openlocfilehash: 8a398eca6da659a6b8f29e4ef8e31b18abf56fde
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357257"
---
# <a name="iserrna-function"></a>Função ISERRNA

Retorna TRUE se o valor de _cellreference_ for o tipo de erro #N/a! (não disponível); caso contrário, retornará FALSE. A função ISERRNA é usada em fórmulas que se referem a outra célula. 
  
## <a name="syntax"></a>Sintaxe

ISERRNA (* * *cellreference* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Obrigatório  <br/> |**String** <br/> |Referência a uma célula.  <br/> |
   
## <a name="example-1"></a>Exemplo 1

|**Cell**|**Fórmula**|**Valor retornado**|
|:-----|:-----|:-----|
|Scratch. a1  <br/> |="5 + 3"  <br/> |8  <br/> |
|Scratch. B1  <br/> |= ISERRNA (Scratch. a1)  <br/> |FALSE  <br/> |
   
Retornará FALSO porque o valor retornado está disponível.
  
## <a name="example-2"></a>Exemplo 2

|**Cell**|**Fórmula**|**Valor retornado**|
|:-----|:-----|:-----|
|Scratch. a1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch. B1  <br/> |= ISERRNA (Scratch. a1)  <br/> |TRUE  <br/> |
   
Retornará VERDADEIRO porque o valor retornado é um tipo de erro de #N/A!
  

