---
title: Função POW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251483
localization_priority: Normal
ms.assetid: c6519c55-5f98-ed0d-95b1-5443d0d23c0b
description: Retorna um número elevado à potência de um expoente.
ms.openlocfilehash: 7a1102aa13f54d7e323247b83af3732ebb63acf4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406308"
---
# <a name="pow-function"></a>Função POW

Retorna um número elevado à potência de um expoente.
  
## <a name="syntax"></a>Sintaxe

POW (* * *número* * *, * * *expoente* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Número** <br/> |O número a ser elevada a potência de um expoente.  <br/> |
| _expoente_ <br/> |Obrigatório  <br/> |**Número** <br/> |O expoente.  <br/> |
   
## <a name="remarks"></a>Comentários

Tanto o _número_ quanto o _expoente_ podem ser não inteiros e podem ser negativos. Se _núm_ não for 0 e _expoente_ for 0, essa função retornará 1. Se _núm_ for 0 e _expoente_ for negativo, essa função retornará 0,0. Se _núm_ e _expoente_ forem 0, ou se _núm_ for negativo e _expoente_ não for um inteiro, essa função retornará 0,0. Se tanto _núm_ quanto _expoente_ forem negativos, essa função retornará-1. #IND. 
  
## <a name="example"></a>Exemplo

POW (5, 2) 
  
Retornará 25. 
  

