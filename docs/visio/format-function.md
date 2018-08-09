---
title: Função FORMAT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251424
localization_priority: Normal
ms.assetid: 52f5ef4d-07c6-ab36-bf74-b30b50eea221
description: Retorna o resultado da expressão como uma cadeia de caracteres formatada de acordo com a figura de formatação.
ms.openlocfilehash: dcb898b3cb21d8cc5ebee7e56540d9e2eefcffdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771936"
---
# <a name="format-function"></a>Função FORMAT

Retorna o resultado da _expressão_ como uma cadeia de caracteres formatada de acordo com a _Figura de formatação_.
  
## <a name="syntax"></a>Sintaxe

FORMATO (* * *expressão* * *, "* * *formatpicture* * *") 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expressão_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma combinação de constantes, operadores, funções e referências a células ShapeSheet que resulta em um valor.  <br/> |
| _Figura de formatação_ <br/> |Obrigatório  <br/> |**String** <br/> |A imagem de formato usada para formatar a cadeia de caracteres.  <br/> |
   
### <a name="return-value"></a>Valor retornado

String
  
## <a name="remarks"></a>Comentários

O tipo da expressão e o tipo especificado na figura de formatação determinam o comportamento de cadeia de caracteres retornada. A _Figura de formatação_ deve ser apropriado para o tipo de expressão. Para obter mais informações sobre como especificar o formato de imagens, consulte [sobre figuras de formatação](about-format-pictures.md).
  
Retorna um erro se o resultado de _expression_ e o tipo esperado em _formatpicture_ forem diferentes ou se há erros de sintaxe em _formatpicture_.
  
## <a name="example-1"></a>Exemplo 1

FORMAT(1cm/4, "0,000 u")
  
Retornará 0,250 cm.
  
## <a name="example-2"></a>Exemplo 2

FORMAT(1cm/4, "0,00 U")
  
Returns "0,25 CM."
  
## <a name="example-3"></a>Exemplo 3

FORMAT(1cm/4, "0,0 u")
  
Returns "0,3 cm."
  

