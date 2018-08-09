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
ms.openlocfilehash: 48870c679251a666a5756b2b684d262fe059eee0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772593"
---
# <a name="pow-function"></a>Função POW

Retorna um número elevado à potência de um expoente.
  
## <a name="syntax"></a>Sintaxe

POW (* * *número* * *, * * *expoente* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Número** <br/> |O número a ser elevada a potência de um expoente.  <br/> |
| _expoente_ <br/> |Obrigatório  <br/> |**Número** <br/> |O expoente.  <br/> |
   
## <a name="remarks"></a>Comentários

_Número_ e o _expoente_ podem ser não-inteiros e devem ser negativos. Se _Núm_ não for 0 e o _expoente_ é 0, essa função retornará 1. Se _Núm_ for 0 e o _expoente_ for negativo, essa função retornará 0,0. Se o _número_ e o _expoente_ vão de 0 ou se _Núm_ for negativo e _expoente_ não for um inteiro, essa função retornará 0,0. Se o _número_ e o _expoente_ forem negativos, essa função retornará -1. #IND. 
  
## <a name="example"></a>Exemplo

POW(5,2) 
  
Retornará 25. 
  

