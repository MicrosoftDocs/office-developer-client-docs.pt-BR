---
title: Função CEILING
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251405
localization_priority: Normal
ms.assetid: 1a8d6d48-7ae3-5483-28d2-5b1706088a53
description: Cerca um número de distância de 0 (zero) para a próxima instância de vários. Se vários não for especificado, o número arredoda para longe de 0 para o próximo inteiro.
ms.openlocfilehash: 449f17d1b68c116cccb2635723a3f6277d0ac2a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404124"
---
# <a name="ceiling-function"></a>Função CEILING

Volta um número de distância de 0 (zero) para a próxima instância de  _vários_. Se  _vários_ não for especificado, o número arredoda para longe de 0 para o próximo inteiro. 
  
## <a name="syntax"></a>Sintaxe

CEILING(** *number* **, ** *multiple* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Número** <br/> |O número a ser arredondado.  <br/> |
| _multiple_ <br/> |Obrigatório  <br/> |**Número** <br/> |O múltiplo para arredondar para.  <br/> |
   
## <a name="remarks"></a>Comentários

 _Número_ e  _múltiplo_ devem ter os mesmos sinais ou um #NUM! será retornado. Se um  _ou_  _vários_ não puderem ser convertidos em um valor, um #VALUE! será retornado. Se um  _ou_  _vários_ for 0, o resultado será 0. 
  
## <a name="example-1"></a>Exemplo 1

CEILING(3,7)
  
Retornará 4
  
## <a name="example-2"></a>Exemplo 2

CEILING(-3,7)
  
Retornará -4
  
## <a name="example-3"></a>Exemplo 3

CEILING(3,7, 0,25)
  
Retornará 3,75
  

