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
description: Arredonda um número para fora de 0 (zero) para a próxima instância de múltiplo. Se múltiplo não for especificado, o número será arredondado para longe de 0 até o próximo inteiro.
ms.openlocfilehash: 449f17d1b68c116cccb2635723a3f6277d0ac2a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337223"
---
# <a name="ceiling-function"></a>Função CEILING

Arredonda um número para fora de 0 (zero) para a próxima instância de _múltiplo_. Se _múltiplo_ não for especificado, o número será arredondado para longe de 0 até o próximo inteiro. 
  
## <a name="syntax"></a>Sintaxe

TETO (* * *número* * *, * * *múltiplo* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Número** <br/> |O número a ser arredondado.  <br/> |
| _vários_ <br/> |Obrigatório  <br/> |**Número** <br/> |O múltiplo a ser arredondado.  <br/> |
   
## <a name="remarks"></a>Comentários

 _Número_ e _múltiplos_ devem ter os mesmos sinais ou um #NUM! será retornado. Se um ou _vários_ _números_ não puderem ser convertidos em um valor, um #VALUE! será retornado. Se um dos _números_ ou _vários_ for 0, o resultado será 0. 
  
## <a name="example-1"></a>Exemplo 1

TETO (3.7)
  
Retornará 4
  
## <a name="example-2"></a>Exemplo 2

TETO (-3,7)
  
Retornará -4
  
## <a name="example-3"></a>Exemplo 3

TETO (3.7, 0,25)
  
Retornará 3,75
  

