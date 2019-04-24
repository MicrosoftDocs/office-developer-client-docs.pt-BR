---
title: Função HSL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251438
localization_priority: Normal
ms.assetid: c9314c39-1d2e-a18f-c01b-8817286099dc
description: Retorna um valor que representa um índice na paleta de cores do documento. Especifica uma cor por seus componentes de matiz, saturação e luminosidade.
ms.openlocfilehash: 55703239395c54beedf4b7383435253f9c37006f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329922"
---
# <a name="hsl-function"></a>Função HSL

Retorna um valor que representa um índice na paleta de cores do documento. Especifica uma cor por seus componentes de matiz, saturação e luminosidade.
  
## <a name="syntax"></a>Sintaxe

HSL (* * *matiz* * *, * * *saturação* * *, * * *luminosidade* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _Tom_ <br/> |Obrigatório  <br/> |**Número** <br/> |A matiz da cor, expressa como um número entre 0 e 239, inclusive, ou uma expressão que é avaliada neste número.  <br/> |
| _saturação_ <br/> |Obrigatório  <br/> |**Número** <br/> |A saturação da cor, expressa como um número entre 0 e 240, inclusive, ou uma expressão que é avaliada neste número.  <br/> |
| _luminosidade_ <br/> |Obrigatório  <br/> |**Número** <br/> | A luminosidade da cor, expressa como um número entre 0 e 240, inclusive, ou uma expressão que é avaliada neste número.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Número
  
## <a name="remarks"></a>Comentários

Se a cor retornada pela função ainda não existir na paleta de cores do documento atual, ela será adicionada à lista de documentos de cores disponíveis. 
  
A tabela a seguir relaciona algumas cores padrão e seus valores de matiz, saturação e luminosidade. 
  
|**Color**|**Valor de matiz**|**Valor de saturação**|**Valor de luminosidade**|
|:-----|:-----|:-----|:-----|
|Preto  <br/> |,0  <br/> |,0  <br/> |dia  <br/> |
|Azul  <br/> |160  <br/> |240  <br/> |120  <br/> |
|Verde  <br/> |80  <br/> |240  <br/> |120  <br/> |
|Ciano  <br/> |120  <br/> |240  <br/> |120  <br/> |
|Vermelho  <br/> |,0  <br/> |240  <br/> |120  <br/> |
|Magenta  <br/> |200  <br/> |240  <br/> |120  <br/> |
|Amarelo  <br/> |40  <br/> |240  <br/> |120  <br/> |
|Branco  <br/> |,0  <br/> |,0  <br/> |240  <br/> |
   
## <a name="example-1"></a>Exemplo 1

HSL (160240120)
  
Retornará o índice da cor azul.
  
## <a name="example-2"></a>Exemplo 2

HSL (matiz (FillForegnd), SAT (FillForegnd), mín (LUM (FillForegnd) + 100240))
  
Retornará o índice de uma cor que espelha a cor de preenchimento de primeiro plano com uma luminosidade crescente.
  

