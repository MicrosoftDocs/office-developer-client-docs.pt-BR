---
title: Função PNT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251480
localization_priority: Normal
ms.assetid: d14a735c-0278-922f-7823-79adf6cb1e64
description: Retorna o ponto representado pelas coordenadas x e y como um único valor.
ms.openlocfilehash: c0a12aa18f4c766ea1f5b0fa1d827804d766713c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322348"
---
# <a name="pnt-function"></a>Função PNT

Retorna o ponto representado pelas coordenadas _x_ e _y_ como um único valor. 
  
## <a name="syntax"></a>Sintaxe

PNT (* * *x, y* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _x, y_ <br/> |Obrigatório  <br/> |**Número, Número** <br/> |As coordenadas do ponto do sistema de coordenadas da forma atual.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Ponto
  
## <a name="remarks"></a>Comentários

A conversão de coordenadas em pontos permite que você altere a geometria de uma forma sem precisar manipular as coordenadas *x* e *y* separadamente. 
  
## <a name="example"></a>Exemplo

PNT (PinX, PinY) 
  
Retornará o ponto representado por PinX e PinY. 
  

