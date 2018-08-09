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
description: Retorna um valor representando um índice na paleta de cores do documento. Especifica uma cor por seu matiz, saturação e luminosidade componentes do.
ms.openlocfilehash: 50f343d990157d831ac4ac43057d0a2b7fca63f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772035"
---
# <a name="hsl-function"></a>Função HSL

Retorna um valor representando um índice na paleta de cores do documento. Especifica uma cor por seu matiz, saturação e luminosidade componentes do.
  
## <a name="syntax"></a>Sintaxe

HSL (* * *matiz* * *, * * *saturação* * *, * * *luminosidade* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _matiz_ <br/> |Obrigatório  <br/> |**Número** <br/> |A matiz da cor, expressa como um número entre 0 e 239, inclusive, ou uma expressão que é avaliada neste número.  <br/> |
| _saturação_ <br/> |Obrigatório  <br/> |**Número** <br/> |A saturação da cor, expressa como um número entre 0 e 240, inclusive, ou uma expressão que é avaliada neste número.  <br/> |
| _luminosidade_ <br/> |Obrigatório  <br/> |**Número** <br/> | A luminosidade da cor, expressa como um número entre 0 e 240, inclusive, ou uma expressão que é avaliada neste número.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Number
  
## <a name="remarks"></a>Comentários

Se a cor retornada pela função ainda não existir na paleta de cores do documento atual, ela será adicionada à lista de documentos de cores disponíveis. 
  
A tabela a seguir relaciona algumas cores padrão e seus valores de matiz, saturação e luminosidade. 
  
|**Color**|**Valor de matiz**|**Valor de saturação**|**Valor de luminosidade**|
|:-----|:-----|:-----|:-----|
|Preto  <br/> |0  <br/> |0  <br/> |24  <br/> |
|Azul  <br/> |160  <br/> |240  <br/> |120  <br/> |
|Verde  <br/> |80  <br/> |240  <br/> |120  <br/> |
|Ciano  <br/> |120  <br/> |240  <br/> |120  <br/> |
|Vermelho  <br/> |0  <br/> |240  <br/> |120  <br/> |
|Magenta  <br/> |200  <br/> |240  <br/> |120  <br/> |
|Amarelo  <br/> |40  <br/> |240  <br/> |120  <br/> |
|Branco  <br/> |0  <br/> |0  <br/> |240  <br/> |
   
## <a name="example-1"></a>Exemplo 1

HSL(160,240,120)
  
Retornará o índice da cor azul.
  
## <a name="example-2"></a>Exemplo 2

HSL(Hue(FillForegnd),Sat(FillForegnd),min(Lum(FillForegnd)+100,240))
  
Retornará o índice de uma cor que espelha a cor de preenchimento de primeiro plano com uma luminosidade crescente.
  

