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
description: Retorna o resultado da expressão como uma cadeia de caracteres formatada de acordo com formatpicture.
ms.openlocfilehash: 5eb2195c2bc52e9cc8e7aa8bc4068826a5cd14c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404649"
---
# <a name="format-function"></a>Função FORMAT

Retorna o resultado da  _expressão como_ uma cadeia de caracteres formatada de acordo com  _formatpicture_.
  
## <a name="syntax"></a>Sintaxe

FORMAT(** *expression* **," ** *formatpicture* ** ") 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma combinação de constantes, operadores, funções e referências a células ShapeSheet que resulta em um valor.  <br/> |
| _formatpicture_ <br/> |Obrigatório  <br/> |**String** <br/> |A imagem de formato usada para formatar a cadeia de caracteres.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Cadeia de caracteres
  
## <a name="remarks"></a>Comentários

O tipo da expressão e o tipo especificado na figura de formatação determinam o comportamento da cadeia de caracteres retornada. A  _formatpicture_ deve ser apropriada para o tipo de expressão. Para obter mais informações sobre como especificar imagens de formato, consulte [Sobre o formato de imagens](about-format-pictures.md).
  
Retorna um erro se  o resultado da expressão e o tipo esperado na _formatação_ são de um tipo diferente ou se houver erros de sintaxe na _formatpicture_.
  
## <a name="example-1"></a>Exemplo 1

FORMAT(1cm/4, "0,000 u")
  
Retornará 0,250 cm.
  
## <a name="example-2"></a>Exemplo 2

FORMAT(1cm/4, "0,00 U")
  
Returns "0,25 CM."
  
## <a name="example-3"></a>Exemplo 3

FORMAT(1cm/4, "0,0 u")
  
Returns "0,3 cm."
  

