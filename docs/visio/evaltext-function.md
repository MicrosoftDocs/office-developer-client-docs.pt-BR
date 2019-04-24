---
title: Função EVALTEXT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251422
localization_priority: Normal
ms.assetid: c9b5b96c-d8c8-6119-e3f1-a2ce9d7c043e
description: Avalia o texto em shapename como se fosse uma fórmula e retorna o resultado.
ms.openlocfilehash: 6600d9d6ddaf630a93fdb5c37639ce50a21a4307
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329047"
---
# <a name="evaltext-function"></a>Função EVALTEXT

Avalia o texto em _shapename_ como se fosse uma fórmula e retorna o resultado. 
  
## <a name="syntax"></a>Sintaxe

EVALTEXT (* * *shapename! o texto* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _shapename! o texto_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma célula é disparada quando a composição do texto da forma associada é alterada.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

String
  
## <a name="remarks"></a>Comentários

 _shapename_ pode ser utilizada para fazer referência ao texto de uma forma que não seja a atual. 
  
Se não tiver texto, o resultado será zero. Se o texto não puder ser avaliado, a função retornará um erro.
  
## <a name="example"></a>Exemplo

EVALTEXT (line. 2! Text) 
  
Avalia o texto contido na forma Line.2. Por exemplo, se Line.2 contiver "4 pés + 0,5 pé", será retornado o valor 4,5 pés. 
  

