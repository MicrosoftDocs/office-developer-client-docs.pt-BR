---
title: Função REPT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027335
localization_priority: Normal
ms.assetid: 53362a32-ac27-42a3-ace1-c6184ab20b52
description: Repete o texto um determinado número de vezes.
ms.openlocfilehash: 761f2f95824d5bdab4995b2867bfeac6be64bc12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772743"
---
# <a name="rept-function"></a>Função REPT

Repete o texto um determinado número de vezes. 
  
## <a name="syntax"></a>Sintaxe

REPT (* * *texto* * *, * * *núm_vezes* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obrigatório  <br/> |**String** <br/> | O texto a ser repetido.  <br/> |
| _núm_vezes_ <br/> |Obrigatório  <br/> |**Número** <br/> |Um número positivo que especifica o número de vezes que o texto será repetido.  <br/> |
   
## <a name="remarks"></a>Comentários

Se *núm_vezes* for: 
  
- For zero (0), REPT retornará "" (texto vazio).
    
- Não for um inteiro, estará truncado.
    
## <a name="example"></a>Exemplo

REPT ("\*", 5) 
  
Retorna \* \* \* \* \*. 
  

