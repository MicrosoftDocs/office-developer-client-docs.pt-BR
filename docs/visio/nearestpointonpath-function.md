---
title: Função NEARESTPOINTONPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Retorna o percentual da distância no caminho do ponto mais próximo às coordenadas especificadas, como um valor entre 0 e 1.
ms.openlocfilehash: ced20cdf1f3531eafaa03c2666b09334029fd3da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407330"
---
# <a name="nearestpointonpath-function"></a>Função NEARESTPOINTONPATH

Retorna o percentual da distância no caminho do ponto mais próximo às coordenadas especificadas, como um valor entre 0 e 1.
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2010
 
  
## <a name="syntax"></a>Sintaxe

NEARESTPOINTONPATH (* * *seção* * *, * * *x* * *, * * *y* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> |A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).  <br/> |
| _x_ <br/> |Obrigatório  <br/> |**Double** <br/> |A coordenada _x_do ponto especificado.  <br/> |
| _y_ <br/> |Obrigatório  <br/> |**Double** <br/> |A coordenada _y_do ponto especificado.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

 **Double**
  
## <a name="remarks"></a>Comentários

Se a _seção_ não existir, o Microsoft Visio retornará #REF!. 
  

