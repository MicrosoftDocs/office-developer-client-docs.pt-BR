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
description: Arredonda um número de 0 (zero), para o próximo número inteiro ou para a próxima instância do múltiplo.
ms.openlocfilehash: f66b993e3ab48fd1abc685b7db5889d5bf24fbfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771889"
---
# <a name="floor-function"></a>Função FLOOR

Arredonda um número de 0 (zero), para o próximo número inteiro ou para a próxima instância do _vários_.
  
## <a name="syntax"></a>Sintaxe

FLOOR (* * *número* * *, * * *vários* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Número** <br/> |O número a ser arredondado.  <br/> |
| _vários_ <br/> |Obrigatório  <br/> |**Número** <br/> |O múltiplo para o qual arredondar.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Number
  
## <a name="remarks"></a>Comentários

Se _vários_ não for especificado, o número será arredondado para 0 do próximo número inteiro. 
  
 _Número_ e _vários_ devem ter o mesmo sinal ou um #NUM! erro será retornado. Se o _número_ ou o _múltiplo_ não puder ser convertida para um valor, um #VALUE! erro será retornado. Se o _número_ ou o _múltiplo_ for 0, o resultado é 0. 
  
## <a name="example-1"></a>Exemplo 1

FLOOR(3.7)
  
Retornará 3.
  
## <a name="example-2"></a>Exemplo 2

FLOOR(-3.7)
  
Retornará -3.
  
## <a name="example-3"></a>Exemplo 3

FLOOR (3,7, 0,5)
  
Retornará 3,5.
  

