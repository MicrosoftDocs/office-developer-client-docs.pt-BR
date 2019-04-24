---
title: Função FORMATEX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251590
localization_priority: Normal
ms.assetid: d375c971-fee2-baa3-dc4f-a26018e70e8a
description: Retorna o resultado da expressão avaliada em srcUnit como uma cadeia de caracteres formatada de acordo com o formato expresso no dstUnit.
ms.openlocfilehash: e341cbcb16cc273f0413f98c195f77ad08946ab1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328627"
---
# <a name="formatex-function"></a>Função FORMATEX

Retorna o resultado da expressão avaliada em srcUnit como uma cadeia de caracteres formatada de acordo com o formato expresso no dstUnit.
  
## <a name="syntax"></a>Sintaxe

FORMATEX (* * *expressão* * *, "* * *formato* * *", [* * *srcUnit* * *], [* * *dstUnit* * *], [* * *LangID* * *] [, * * *calID* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expressão_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma combinação de constantes, operadores, funções e referências a células ShapeSheet que resulta em um valor.  <br/> |
| _format_ <br/> |Obrigatório  <br/> |**String** <br/> |A imagem de formato usada para formatar a cadeia de caracteres. Para obter mais informações sobre como formatar imagens, consulte [about Format Pictures](about-format-pictures.md).  <br/> |
| _srcUnit_ <br/> |Opcional  <br/> |**String** <br/> | Unidades usadas para avaliar a expression (pol, cm, etc.).  <br/> |
| _dstUnit_ <br/> |Opcional  <br/> |**String** <br/> |Unidades usadas para o resultado de expression (pol, cm, etc.).  <br/> |
| _Lang_ <br/> |Opcional  <br/> |**Número** <br/> |O idioma usado ao formatar as imagens de data/hora do Microsoft Office System.  <br/> |
| _calID_ <br/> |Opcional  <br/> |**Número** <br/> |O calendário usado ao formatar as imagens de data/hora do Microsoft Office System.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

String
  
## <a name="remarks"></a>Comentários

O tipo da expressão e o tipo especificado na figura de formatação determinam o comportamento da cadeia de caracteres retornada. O format deve ser adequado para o texto da expressão.
  
O argumento srcUnit é usado para dimensionar resultados de expressão não digitada, como 3 + 4. Se o resultado de expression possuir um texto explícito, como 3 pés + 8 pés, então srcUnit será ignorada.
  
O argumento dstUnit é usado para especificar as unidades usadas para o resultado formatado. Se dstUnit não for especificado, as unidades para o resultado da expressão serão usadas.
  
Retorna um erro se o resultado de expression e o texto esperado em format forem de um tipo diferente, se houver erros de sintaxe em format ou se as unidades srcUnit ou dstUnit não forem reconhecidas.
  
## <a name="example"></a>Exemplo

FORMATEX(5,5, "0,00 u", "cm", "pés") 
  
Retorna 0,18 pés. 
  

