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
description: Retorna um valor que representa um índice na paleta de cores do documento. Especifica uma cor por seus componentes vermelho, verde e azul, onde cada um é um número no intervalo de 0 a 255, inclusive, ou uma expressão que é avaliada como um número.
ms.openlocfilehash: 34f9c2f2043afe6144feba561e545dc7be35a5a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326737"
---
# <a name="rgb-function-visioshapesheet"></a>Função RGB (VisioShapeSheet)

Retorna um valor que representa um índice na paleta de cores do documento. Especifica uma cor por seus componentes vermelho, verde e azul, onde cada um é um número no intervalo de 0 a 255, inclusive, ou uma expressão que é avaliada como um número. 
  
## <a name="syntax"></a>Sintaxe

RGB (* * *vermelho* * *, * * *verde* * *, * * *azul* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _vermelha_ <br/> |Obrigatório  <br/> |**Número** <br/> |O componente vermelho.  <br/> |
| _natureza_ <br/> |Obrigatório  <br/> |**Número** <br/> |O componente verde.  <br/> |
| _azuis_ <br/> |Obrigatório  <br/> |**Nmber** <br/> |O componente azul.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Número
  
## <a name="remarks"></a>Comentários

Se a cor retornada pela função ainda não existir na paleta de cores do documento atual, ela será adicionada à paleta.
  
A tabela a seguir relaciona algumas cores padrão e seus valores de vermelho, verde e azul.
  
|**Color**|**Valor de vermelho**|**Valor de verde**|**Valor de azul**|
|:-----|:-----|:-----|:-----|
|Preto  <br/> |,0  <br/> |,0  <br/> |,0  <br/> |
|Azul  <br/> |,0  <br/> |,0  <br/> |255  <br/> |
|Verde  <br/> |,0  <br/> |255  <br/> |,0  <br/> |
|Ciano  <br/> |,0  <br/> |255  <br/> |255  <br/> |
|Vermelho  <br/> |255  <br/> |,0  <br/> |,0  <br/> |
|Magenta  <br/> |255  <br/> |,0  <br/> |255  <br/> |
|Amarelo  <br/> |255  <br/> |255  <br/> |,0  <br/> |
|Branco  <br/> |255  <br/> |255  <br/> |255  <br/> |
   
## <a name="example-1"></a>Exemplo 1

RGB (0, 0255)
  
Retornará o índice da cor azul.
  
## <a name="example-2"></a>Exemplo 2

RGB (vermelho (planilha. 1! FillForegnd), 120, 0)
  
Retornará o índice de uma cor cujo componente vermelho espelhe o primeiro plano de preenchimento de Sheet.1.
  

