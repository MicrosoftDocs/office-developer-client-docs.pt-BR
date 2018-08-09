---
title: Função ISERR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251448
localization_priority: Normal
ms.assetid: 87508007-8ad2-3bcf-55dc-f0207c7c6fe3
description: 'Retorna VERDADEIRO se o valor de referênciadecélula for qualquer tipo de erro exceto # n/d; Caso contrário, ele retornará FALSE. A função ISERR é usada em fórmulas que se referem a outra célula.'
ms.openlocfilehash: 651b095e53b7f2690aa9c8774d87d5afcede75be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772098"
---
# <a name="iserr-function"></a>Função ISERR

Retorna TRUE se o valor de _referênciadecélula_ for qualquer tipo de erro exceto # n/d; Caso contrário, ele retornará FALSE. A função ISERR é usada em fórmulas que se referem a outra célula. 
  
## <a name="syntax"></a>Sintaxe

ÉERRO (* * *referênciadecélula* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _referênciadecélula_ <br/> |Obrigatório  <br/> |**String** <br/> |Referência a uma célula.  <br/> |
   
## <a name="example-1"></a>Exemplo 1

|**Célula**|**Formula**|**Valor retornado**|
|:-----|:-----|:-----|
|Scratch. a1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERR(Scratch.a1)  <br/> |FALSO  <br/> |
   
Retornará FALSO porque o erro de #N/A! não é reconhecido pela função ISERR. Utilize a função ISERROR para localizar todos os tipos de erros.
  
## <a name="example-2"></a>Exemplo 2

|**Célula**|**Formula**|**Valor retornado**|
|:-----|:-----|:-----|
|Y1  <br/> |="Casa"  <br/> |#VALUE!  <br/> |
|Scratch. a1  <br/> |=ISERR(Scratch.x1)  <br/> |VERDADEIRO  <br/> |
   
Retornará VERDADEIRO porque o erro de #VALUE! é reconhecido pela função ISERR.
  

