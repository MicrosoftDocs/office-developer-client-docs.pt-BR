---
title: Função FLOOR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
localization_priority: Normal
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: Arredoda um número em direção a 0 (zero), para o próximo inteiro ou para a próxima instância de vários.
ms.openlocfilehash: 7a16a77a990180f34dd7a5706c24ec3232438467
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439895"
---
# <a name="floor-function"></a>Função FLOOR

Arredoda um número em direção a 0 (zero), para o próximo inteiro ou para a próxima instância de  _vários_.
  
## <a name="syntax"></a>Sintaxe

FLOOR(** *number* **, ** *multiple* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Número** <br/> |O número a ser arredondado.  <br/> |
| _multiple_ <br/> |Obrigatório  <br/> |**Número** <br/> |O múltiplo para o qual arredondar.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Número
  
## <a name="remarks"></a>Comentários

Se  _vários_ não for especificado, o número arredoda em direção a 0 para o próximo inteiro. 
  
 _Número_ e  _múltiplo_ devem ter os mesmos sinais ou um #NUM! será retornado. Se um  _ou_  _vários_ não puderem ser convertidos em um valor, uma #VALUE! será retornado. Se um  _ou_  _vários_ for 0, o resultado será 0. 
  
## <a name="example-1"></a>Exemplo 1

FLOOR(3,7)
  
Retornará 3.
  
## <a name="example-2"></a>Exemplo 2

FLOOR(-3,7)
  
Retornará -3.
  
## <a name="example-3"></a>Exemplo 3

FLOOR(3.7, 0.5)
  
Retornará 3,5.
  

