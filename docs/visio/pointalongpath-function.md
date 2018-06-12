---
title: Função POINTALONGPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: Retorna as coordenadas de um ponto no caminho ou o deslocamento em relação a ele.
ms.openlocfilehash: 9ce6f8c171515b46aaff0ce07cbe7da4f1e958d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772513"
---
# <a name="pointalongpath-function"></a>Função POINTALONGPATH

Retorna as coordenadas de um ponto no caminho ou o deslocamento em relação a ele.
  
## <a name="version-information"></a>Informações da versão

Versão adicionada: Visio 2010 
  
## <a name="syntax"></a>Sintaxe

POINTALONGPATH (* * *seção* * *, * * *de viagem* * * * * *[, deslocamento]* * * * * *[, segmento]* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obrigatório  <br/> |**String** <br/> |A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).  <br/> |
| _viagem_ <br/> |Obrigatório  <br/> |**Double** <br/> |O percentual do caminho percorrido, do ponto inicial ao ponto final, que identifica o ponto. Deve estar entre 0 e 1.  <br/> |
| _deslocamento_ <br/> |Opcional  <br/> |**Double** <br/> |A distância que esse ponto é deslocado do caminho. Consulte Comentários para obter mais informações.  <br/> |
| _segmento_ <br/> |Opcional  <br/> |**Integer** <br/> |O segmento baseado em 1 do caminho no qual as coordenadas deverão ser calculadas.  <br/> |
   
### <a name="return-value"></a>Valor retornado

 **Ponto**
  
## <a name="remarks"></a>Coment�rios

Se não existir _section_ nem _segment_ , o Microsoft Visio retornará #REF!. 
  
Valores de *deslocamento* de positivos especificam pontos à esquerda da direção da viagem. 
  
Valores de *deslocamento* de negativos especificam pontos à direita da direção da viagem. 
  
Um **Point** representa um par ordenado de coordenadas geométricas (*x, y*) como um valor único. 
  

