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
description: 'Retorna TRUE se o valor de cellreference for qualquer tipo de erro, exceto #N/A; caso contrário, retornará FALSE. A função ISERR é usada em fórmulas que se referem a outra célula.'
ms.openlocfilehash: e2117c38d3cad2408295ed6894aefc78e107596e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432104"
---
# <a name="iserr-function"></a>Função ISERR

Retorna VERDADEIRO se o valor de  _cellreference for_ qualquer tipo de erro, exceto #N/A; caso contrário, retornará FALSE. A função ISERR é usada em fórmulas que se referem a outra célula. 
  
## <a name="syntax"></a>Sintaxe

ISERR(** *cellreference* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Obrigatório  <br/> |**String** <br/> |Referência a uma célula.  <br/> |
   
## <a name="example-1"></a>Exemplo 1

|**Cell**|**Fórmula**|**Valor retornado**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERR(Scratch.A1)  <br/> |FALSE  <br/> |
   
Retornará FALSO porque o erro de #N/A! não é reconhecido pela função ISERR. Utilize a função ISERROR para localizar todos os tipos de erros.
  
## <a name="example-2"></a>Exemplo 2

|**Cell**|**Fórmula**|**Valor retornado**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="House"  <br/> |#VALUE!  <br/> |
|Scratch.A1  <br/> |=ISERR(Scratch.X1)  <br/> |TRUE  <br/> |
   
Retornará VERDADEIRO porque o erro de #VALUE! é reconhecido pela função ISERR.
  

