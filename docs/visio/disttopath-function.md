---
title: Função DISTTOPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: Retorna a distância mais curta do ponto representado pelas coordenadas especificadas até um ponto no caminho.
ms.openlocfilehash: 5727b24739705d3e562150c48fe77f7ad6eedb57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427014"
---
# <a name="disttopath-function"></a>Função DISTTOPATH

Retorna a distância mais curta do ponto representado pelas coordenadas especificadas até um ponto no caminho.
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2010
 
  
## <a name="syntax"></a>Sintaxe

DISTTOPATH(** *seção* **, ** *x* **, ** *y* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obrigatório  <br/> |**String** <br/> |A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).  <br/> |
| _x_ <br/> |Obrigatório  <br/> |**Double** <br/> |A  _coordenada x_ do ponto.  <br/> |
| _y_ <br/> |Obrigatório  <br/> |**Double** <br/> |A  _coordenada y_ do ponto.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

 **Double**
  
## <a name="remarks"></a>Comentários

O Microsoft Visio retornará #REF! se  _a_ seção não existir. 
  
O valor retornado será positivo se o ponto estiver à esquerda da direção da viagem e negativo caso esteja à direita.
  

