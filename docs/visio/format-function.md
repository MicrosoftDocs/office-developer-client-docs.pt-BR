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
description: Retorna o resultado da expressão como uma cadeia de caracteres formatada de acordo com o formatPicture.
ms.openlocfilehash: 5eb2195c2bc52e9cc8e7aa8bc4068826a5cd14c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339890"
---
# <a name="format-function"></a>Função FORMAT

Retorna o resultado da _expressão_ como uma cadeia de caracteres formatada de acordo com o _formatPicture_.
  
## <a name="syntax"></a>Sintaxe

Formato (* * *expressão* * *, "* * *formatPicture* * *") 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expressão_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma combinação de constantes, operadores, funções e referências a células ShapeSheet que resulta em um valor.  <br/> |
| _formatPicture_ <br/> |Obrigatório  <br/> |**String** <br/> |A imagem de formato usada para formatar a cadeia de caracteres.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

String
  
## <a name="remarks"></a>Comentários

O tipo da expressão e o tipo especificado na figura de formatação determinam o comportamento da cadeia de caracteres retornada. O _formatPicture_ deve ser apropriado para o tipo de expressão. Para obter mais informações sobre como especificar imagens de formato, consulte [about Format Pictures](about-format-pictures.md).
  
Retorna um erro se o resultado da _expressão_ e o tipo esperado em _formatPicture_ forem de um tipo diferente ou se houver erros de sintaxe no _formatPicture_.
  
## <a name="example-1"></a>Exemplo 1

FORMAT(1cm/4, "0,000 u")
  
Retornará 0,250 cm.
  
## <a name="example-2"></a>Exemplo 2

FORMAT(1cm/4, "0,00 U")
  
Returns "0,25 CM."
  
## <a name="example-3"></a>Exemplo 3

FORMAT(1cm/4, "0,0 u")
  
Returns "0,3 cm."
  

