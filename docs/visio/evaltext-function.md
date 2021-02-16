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
description: Avalia o texto no nome da forma como se fosse uma fórmula e retorna o resultado.
ms.openlocfilehash: 6600d9d6ddaf630a93fdb5c37639ce50a21a4307
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438355"
---
# <a name="evaltext-function"></a>Função EVALTEXT

Avalia o texto no  _nome da forma_ como se fosse uma fórmula e retorna o resultado. 
  
## <a name="syntax"></a>Sintaxe

EVALTEXT(** *shapename!theText* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _shapename!theText_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma célula é disparada quando a composição do texto da forma associada é alterada.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Cadeia de caracteres
  
## <a name="remarks"></a>Comentários

 _shapename_ pode ser utilizada para fazer referência ao texto de uma forma que não seja a atual. 
  
Se não tiver texto, o resultado será zero. Se o texto não puder ser avaliado, a função retornará um erro.
  
## <a name="example"></a>Exemplo

EVALTEXT(Line.2!theText) 
  
Avalia o texto contido na forma Line.2. Por exemplo, se Line.2 contiver "4 pés + 0,5 pé", será retornado o valor 4,5 pés. 
  

