---
title: Função NEARESTPOINTONPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Retorna o percentual da distância no caminho do ponto mais próximo às coordenadas especificadas, como um valor entre 0 e 1.
ms.openlocfilehash: d9e9b890033526fec99f04cee30ae93578487652
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772404"
---
# <a name="nearestpointonpath-function"></a>Função NEARESTPOINTONPATH

Retorna o percentual da distância no caminho do ponto mais próximo às coordenadas especificadas, como um valor entre 0 e 1.
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2010
 
  
## <a name="syntax"></a>Sintaxe

NEARESTPOINTONPATH (* * *seção* * *, * * *x* * *, * * *y* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obrigatório  <br/> |**String** <br/> |A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).  <br/> |
| _x_ <br/> |Obrigatório  <br/> |**Double** <br/> |_X_-coordenadas do ponto especificado.  <br/> |
| _y_ <br/> |Obrigatório  <br/> |**Double** <br/> |_Y_-coordenadas do ponto especificado.  <br/> |
   
### <a name="return-value"></a>Valor retornado

 **Double**
  
## <a name="remarks"></a>Comentários

Se a _seção_ não existir, o Microsoft Visio retornará #REF!. 
  

