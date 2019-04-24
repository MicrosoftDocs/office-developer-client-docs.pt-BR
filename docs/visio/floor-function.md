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
description: Arredonda um número para 0 (zero), para o próximo inteiro ou para a próxima instância de múltiplo.
ms.openlocfilehash: 7a16a77a990180f34dd7a5706c24ec3232438467
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346176"
---
# <a name="floor-function"></a>Função FLOOR

Arredonda um número para 0 (zero), para o próximo inteiro ou para a próxima instância de _múltiplo_.
  
## <a name="syntax"></a>Sintaxe

PISO (* * *número* * *, * * *múltiplo* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Número** <br/> |O número a ser arredondado.  <br/> |
| _vários_ <br/> |Obrigatório  <br/> |**Número** <br/> |O múltiplo para o qual arredondar.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Número
  
## <a name="remarks"></a>Comentários

Se _múltiplo_ não for especificado, o número será arredondado para 0 até o próximo inteiro. 
  
 _Número_ e _múltiplos_ devem ter os mesmos sinais ou um #NUM! será retornado. Se um ou _vários_ _números_ não puderem ser convertidos em um valor, um #VALUE! será retornado. Se um dos _números_ ou _vários_ for 0, o resultado será 0. 
  
## <a name="example-1"></a>Exemplo 1

PISO (3.7)
  
Retornará 3.
  
## <a name="example-2"></a>Exemplo 2

FLOOR (-3,7)
  
Retornará -3.
  
## <a name="example-3"></a>Exemplo 3

PISO (3.7, 0,5)
  
Retornará 3,5.
  

