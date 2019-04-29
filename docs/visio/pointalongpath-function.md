---
title: Função POINTALONGPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: Retorna as coordenadas de um ponto no caminho ou o deslocamento em relação a ele.
ms.openlocfilehash: ce8b54bbd821cbfa6eb1f2789193ff8d7dda42d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430480"
---
# <a name="pointalongpath-function"></a>Função POINTALONGPATH

Retorna as coordenadas de um ponto no caminho ou o deslocamento em relação a ele.
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2010
 
  
## <a name="syntax"></a>Sintaxe

POINTALONGPATH (* * *seção* * *, * * *viagem* * * * * *[, deslocamento]* * * * * *[, segmento]* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> |A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).  <br/> |
| _transmiti_ <br/> |Obrigatório  <br/> |**Double** <br/> |O percentual do caminho percorrido, do ponto inicial ao ponto final, que identifica o ponto. Deve estar entre 0 e 1.  <br/> |
| _partida_ <br/> |Opcional  <br/> |**Double** <br/> |A distância que esse ponto é deslocado do caminho. Consulte Comentários para obter mais informações.  <br/> |
| _segmento_ <br/> |Opcional  <br/> |**Integer** <br/> |O segmento baseado em 1 do caminho no qual as coordenadas deverão ser calculadas.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

 **Point**
  
## <a name="remarks"></a>Comentários

Se a _seção_ ou o _segmento_ não existir, o Microsoft Visio retornará #REF!. 
  
Valores de *deslocamento* positivos especificam pontos à esquerda da direção da viagem. 
  
Valores de *deslocamento* negativos especificam pontos à direita da direção da viagem. 
  
Um **Point** representa um par ordenado de coordenadas geométricas (*x,y*) como um único valor. 
  

