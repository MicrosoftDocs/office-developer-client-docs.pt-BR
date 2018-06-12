---
title: Função ANGLEALONGPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Retorna o ângulo da tangente para o caminho em um determinado ponto.
ms.openlocfilehash: ec5529037275fc8661972cc7403886cd33150b38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771289"
---
# <a name="anglealongpath-function"></a>Função ANGLEALONGPATH

Retorna o ângulo da tangente para o caminho em um determinado ponto.
  
## <a name="version-information"></a>Informações da versão

Versão adicionada: Visio 2010 
  
## <a name="syntax"></a>Sintaxe

ANGLEALONGPATH (* * *seção* * *, * * *de viagem* * * * * *[, segmento]* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obrigatório  <br/> |**String** <br/> |A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).  <br/> |
| _viagem_ <br/> |Obrigatório  <br/> |**Double** <br/> |O percentual no caminho do ponto inicial ao ponto final. Deve estar entre 0 e 1.  <br/> |
| _segmento_ <br/> |Opcional  <br/> |**Integer** <br/> |O segmento baseado em 1 do caminho no qual o ângulo da tangente deverá ser calculado.  <br/> |
   
### <a name="return-value"></a>Valor retornado

 **Double**
  
## <a name="remarks"></a>Coment�rios

Se você incluir um valor _segment_ , ANGLEALONGPATH retornará o valor para esse segmento apenas. 
  
Se você incluir um valor _segment_ , ANGLEALONGPATH determinará o ponto da tangente usando _viajam_ para calcular o percentual em _segment_.
  
Se não existir _section_ nem _segment_ , o Microsoft Visio retornará #REF!. 
  

