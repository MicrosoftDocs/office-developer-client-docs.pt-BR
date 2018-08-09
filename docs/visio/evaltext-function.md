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
description: Avalia o texto no shapename como se fosse uma fórmula e retorna o resultado.
ms.openlocfilehash: 69e79a23faa9d09aa2ad51f83363064b54742152
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771819"
---
# <a name="evaltext-function"></a>Função EVALTEXT

Avalia o texto no _shapename_ como se fosse uma fórmula e retorna o resultado. 
  
## <a name="syntax"></a>Sintaxe

EVALTEXT (* * *shapename! theText* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _shapename! theText_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma célula é disparada quando a composição do texto da forma associada é alterada.  <br/> |
   
### <a name="return-value"></a>Valor retornado

String
  
## <a name="remarks"></a>Comentários

 _shapename_ pode ser utilizada para fazer referência ao texto de uma forma que não seja a atual. 
  
Se não tiver texto, o resultado será zero. Se o texto não puder ser avaliado, a função retornará um erro.
  
## <a name="example"></a>Exemplo

EVALTEXT(line.2!theText) 
  
Avalia o texto contido na forma Line.2. Por exemplo, se Line.2 contiver "4 pés + 0,5 pé", será retornado o valor 4,5 pés. 
  

