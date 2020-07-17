---
title: Função ANGLEALONGPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Retorna o ângulo da tangente para o caminho em um determinado ponto.
ms.openlocfilehash: a15e45ff6135972cd1cd78382147a493f8fc8d69
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160290"
---
# <a name="anglealongpath-function"></a>Função ANGLEALONGPATH

Retorna o ângulo da tangente para o caminho em um determinado ponto.
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2010
 
  
## <a name="syntax"></a>Sintaxe

ANGLEALONGPATH (***seção***, ***viagem*** ***[, segmento]*** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obrigatório  <br/> |**String** <br/> |A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).  <br/> |
| _transmiti_ <br/> |Obrigatório  <br/> |**Double** <br/> |O percentual no caminho do ponto inicial ao ponto final. Deve estar entre 0 e 1.  <br/> |
| _segmento_ <br/> |Opcional  <br/> |**Integer** <br/> |O segmento baseado em 1 do caminho no qual o ângulo da tangente deverá ser calculado.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

 **Double**
  
## <a name="remarks"></a>Comentários

Se você incluir um valor de _segmento_ , ANGLEALONGPATH retornará o valor somente para esse segmento. 
  
Se você incluir um valor de _segmento_ , ANGLEALONGPATH determina o ponto da tangente usando a _viagem_ para calcular a percertment ao longo do _segmento_.
  
Se qualquer _seção_ ou _segmento_ não existir, o Microsoft Visio retornará #REF!. 
  

