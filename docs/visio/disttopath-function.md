---
title: Função DISTTOPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: Retorna a distância mais curta do ponto representado pelas coordenadas especificadas até um ponto no caminho.
ms.openlocfilehash: 227fe860de2e3683b5d7d3e5f9313d1e2e31b2d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771747"
---
# <a name="disttopath-function"></a>Função DISTTOPATH

Retorna a distância mais curta do ponto representado pelas coordenadas especificadas até um ponto no caminho.
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2010
 
  
## <a name="syntax"></a>Sintaxe

DISTTOPATH (* * *seção* * *, * * *x* * *, * * *y* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obrigatório  <br/> |**String** <br/> |A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).  <br/> |
| _x_ <br/> |Obrigatório  <br/> |**Double** <br/> |_X_-coordenadas do ponto.  <br/> |
| _y_ <br/> |Obrigatório  <br/> |**Double** <br/> |_Y_-coordenadas do ponto.  <br/> |
   
### <a name="return-value"></a>Valor retornado

 **Double**
  
## <a name="remarks"></a>Comentários

O Microsoft Visio retornará #REF! Se não existir _section_ . 
  
O valor retornado será positivo se o ponto estiver à esquerda da direção da viagem e negativo caso esteja à direita.
  

