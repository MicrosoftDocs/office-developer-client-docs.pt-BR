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
description: 'Retorna TRUE se o valor de referênciadecélula for o tipo de erro # n/d! (não disponível); Caso contrário, ele retornará FALSE. A função ISERRNA é usada em fórmulas que se referem a outra célula.'
ms.openlocfilehash: a471119265d77866e51ccc6bb556f2ce0095d31d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772110"
---
# <a name="iserrna-function"></a>Função ISERRNA

Retorna TRUE se o valor de _referênciadecélula_ for o tipo de erro # n/d! (não disponível); Caso contrário, ele retornará FALSE. A função ISERRNA é usada em fórmulas que se referem a outra célula. 
  
## <a name="syntax"></a>Sintaxe

ISERRNA (* * *referênciadecélula* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _referênciadecélula_ <br/> |Obrigatório  <br/> |**String** <br/> |Referência a uma célula.  <br/> |
   
## <a name="example-1"></a>Exemplo 1

|**Célula**|**Formula**|**Valor retornado**|
|:-----|:-----|:-----|
|Scratch. a1  <br/> |="5 + 3"  <br/> |"8"  <br/> |
|Scratch.B1  <br/> |=ISERRNA(Scratch.a1)  <br/> |FALSO  <br/> |
   
Retornará FALSO porque o valor retornado está disponível.
  
## <a name="example-2"></a>Exemplo 2

|**Célula**|**Formula**|**Valor retornado**|
|:-----|:-----|:-----|
|Scratch. a1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERRNA(Scratch.a1)  <br/> |VERDADEIRO  <br/> |
   
Retornará VERDADEIRO porque o valor retornado é um tipo de erro de #N/A!
  

