---
title: Função RGB (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251489
localization_priority: Normal
ms.assetid: f6b9f65c-6752-16cb-7eb1-44e1ce56e80b
description: Retorna um valor representando um índice na paleta de cores do documento. Especifica uma cor por seus componentes vermelhos, verdes e azuis, onde cada uma é um número no intervalo de 0 a 255, inclusive, ou uma expressão que é avaliada neste número.
ms.openlocfilehash: 7fa129d3ed28441f619660ed0db035cde85979bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772725"
---
# <a name="rgb-function-visioshapesheet"></a>Função RGB (VisioShapeSheet)

Retorna um valor representando um índice na paleta de cores do documento. Especifica uma cor por seus componentes vermelhos, verdes e azuis, onde cada uma é um número no intervalo de 0 a 255, inclusive, ou uma expressão que é avaliada neste número. 
  
## <a name="syntax"></a>Sintaxe

RGB (* * *vermelho* * *, * * *verde* * *, * * *azul* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _vermelho_ <br/> |Obrigatório  <br/> |**Número** <br/> |O componente vermelho.  <br/> |
| _verde_ <br/> |Obrigatório  <br/> |**Número** <br/> |O componente verde.  <br/> |
| _azul_ <br/> |Obrigatório  <br/> |**Número** <br/> |O componente azul.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Number
  
## <a name="remarks"></a>Comentários

Se a cor retornada pela função ainda não existir na paleta de cores do documento atual, ela será adicionada à paleta.
  
A tabela a seguir relaciona algumas cores padrão e seus valores de vermelho, verde e azul.
  
|**Color**|**Valor de vermelho**|**Valor de verde**|**Valor de azul**|
|:-----|:-----|:-----|:-----|
|Preto  <br/> |0  <br/> |0  <br/> |0  <br/> |
|Azul  <br/> |0  <br/> |0  <br/> |255  <br/> |
|Verde  <br/> |0  <br/> |255  <br/> |0  <br/> |
|Ciano  <br/> |0  <br/> |255  <br/> |255  <br/> |
|Vermelho  <br/> |255  <br/> |0  <br/> |0  <br/> |
|Magenta  <br/> |255  <br/> |0  <br/> |255  <br/> |
|Amarelo  <br/> |255  <br/> |255  <br/> |0  <br/> |
|Branco  <br/> |255  <br/> |255  <br/> |255  <br/> |
   
## <a name="example-1"></a>Exemplo 1

RGB(0,0,255)
  
Retornará o índice da cor azul.
  
## <a name="example-2"></a>Exemplo 2

RGB (vermelho (Sheet.1! FillForegnd), 120, 0)
  
Retornará o índice de uma cor cujo componente vermelho espelhe o primeiro plano de preenchimento de Sheet.1.
  

