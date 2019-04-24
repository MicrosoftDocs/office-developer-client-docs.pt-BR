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
description: Repete um texto um determinado número de vezes.
ms.openlocfilehash: 84e7167fcee426c607e6967aff0530362685dd35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326800"
---
# <a name="rept-function"></a>Função REPT

Repete um texto um determinado número de vezes. 
  
## <a name="syntax"></a>Sintaxe

REPT (* * *texto* * *, * * *number_times* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obrigatório  <br/> |**String** <br/> | O texto a ser repetido.  <br/> |
| _number_times_ <br/> |Obrigatório  <br/> |**Número** <br/> |Um número positivo que especifica o número de vezes que o texto será repetido.  <br/> |
   
## <a name="remarks"></a>Comentários

Se *number_times* for: 
  
- For zero (0), REPT retornará "" (texto vazio).
    
- Não for um inteiro, estará truncado.
    
## <a name="example"></a>Exemplo

REPT ("\*", 5) 
  
\* \*Retorna \*. \* \* 
  

