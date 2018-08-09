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
description: Retorna TRUE se o valor de referênciadecélula for qualquer tipo de erro; Caso contrário, ele retornará FALSE. A função ISERROR é usada em fórmulas que se referem a outra célula.
ms.openlocfilehash: c93801f5d61e45be5d178027405ead3aa129654d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772112"
---
# <a name="iserror-function-visioshapesheet"></a>Função ISERROR (VisioShapeSheet)

Retorna TRUE se o valor de _referênciadecélula_ for qualquer tipo de erro; Caso contrário, ele retornará FALSE. A função ISERROR é usada em fórmulas que se referem a outra célula. 
  
## <a name="syntax"></a>Sintaxe

ISERROR (* * *referênciadecélula* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _referênciadecélula_ <br/> |Obrigatório  <br/> |**String** <br/> |Referência a uma célula.  <br/> |
   
## <a name="example-1"></a>Exemplo 1

|**Célula**|**Formula**|**Valor retornado**|
|:-----|:-----|:-----|
|Scratch. a1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=IsError(Scratch.a1)  <br/> |VERDADEIRO  <br/> |
   
Retornará VERDADEIRO porque o erro de #N/A! é reconhecido pela função ISERROR. Utilize a função ISERR para localizar todos os tipos de erro, exceto #N/A!.
  
## <a name="example-2"></a>Exemplo 2

|**Célula**|**Formula**|**Valor retornado**|
|:-----|:-----|:-----|
|Y1  <br/> |="Casa"  <br/> |#VALUE!  <br/> |
|Scratch.B1  <br/> |=IsError(Scratch.x1)  <br/> |VERDADEIRO  <br/> |
   
Retornará VERDADEIRO porque o erro de #VALUE! é reconhecido pela função ISERROR. Para criar uma expressão com base no erro de #VALUE!, utilize a função ISERRVALUE.
  

